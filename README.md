# Repository


public void ConfigureServices(IServiceCollection services)
{
    services.AddTransient<IUnitOfWork, UnitOfWork>();
}


private IUnitOfWork uw;
public HomeController(IUnitOfWork unitOfWork)
{
    uw = unitOfWork;
}
uw.ClinicRepository<Cities>().FindAll()
