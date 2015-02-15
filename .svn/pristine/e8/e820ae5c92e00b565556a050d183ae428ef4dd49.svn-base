using System;
using System.Collections.Generic;
using System.Configuration;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Shapes;

namespace NetDeckNavigator
{
	/// <summary>
	/// Interaction logic for Options.xaml
	/// </summary>
	public partial class Options : Window
	{
		public Options()
		{
			InitializeComponent();
			this.txtBoxBuildSpeed.Text = ConfigurationManager.AppSettings["BuildSpeed"];
			this.txtBoxUserName.Text = ConfigurationManager.AppSettings["HearthPwnUserName"];
		}

		public void SavePreferences(object sender, RoutedEventArgs e)
		{
			Configuration config = ConfigurationManager.OpenExeConfiguration(ConfigurationUserLevel.None);
			config.AppSettings.Settings["HearthPwnUserName"].Value = this.txtBoxUserName.Text;
			config.AppSettings.Settings["BuildSpeed"].Value = this.txtBoxBuildSpeed.Text;
			config.Save();
			ConfigurationManager.RefreshSection("appSettings");
		}
	}
}
