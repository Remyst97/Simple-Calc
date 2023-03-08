# Simple-Calc
#Initialize application on MyForm.cpp:

	#include "MyForm.h"
	using namespace System;
	using namespace System::Windows::Forms;

	[STAThread]
	void Main(array<String^>^ args)
	{
 	   Application::EnableVisualStyles();
  	  Application::SetCompatibleTextRenderingDefault(false);
  	  Calcalate::MyForm form;
    	  Application::Run(% form);
	}

#Design form with two text with for variables, empty lable and four buttons for the functions on MyForm.h [Design]. // ![image](https://user-images.githubusercontent.com/127352211/223856722-1940bd46-8f6e-418f-9d7c-93bb18c5c07d.png)

#Code for the design of my Calculator on MyForm.h:

	#pragma once

	namespace Calcalate {

		using namespace System;
		using namespace System::ComponentModel;
		using namespace System::Collections;
		using namespace System::Windows::Forms;
		using namespace System::Data;
		using namespace System::Drawing;

		/// <summary>
		/// Summary for MyForm
		/// </summary>
		public ref class MyForm : public System::Windows::Forms::Form
		{
		public:
			MyForm(void)
			{
				InitializeComponent();
				//
				//TODO: Add the constructor code here
				//
			}

		protected:
			/// <summary>
			/// Clean up any resources being used.
			/// </summary>
			~MyForm()
			{
				if (components)
				{
					delete components;
				}
			}
		private: System::Windows::Forms::TextBox^ variable1;
		protected:

		protected:

		private: System::Windows::Forms::Label^ function;
		private: System::Windows::Forms::TextBox^ variable2;
		private: System::Windows::Forms::Button^ addition;
		private: System::Windows::Forms::Button^ subtraction;
		private: System::Windows::Forms::Button^ multiply;
		private: System::Windows::Forms::Button^ division;
		private: System::Windows::Forms::Label^ result;
		private: System::Windows::Forms::Label^ total;


		protected:

		private:
			/// <summary>
			/// Required designer variable.
			/// </summary>
			System::ComponentModel::Container ^components;

	#pragma region Windows Form Designer generated code
			/// <summary>
			/// Required method for Designer support - do not modify
			/// the contents of this method with the code editor.
			/// </summary>
			void InitializeComponent(void)
			{
				this->variable1 = (gcnew System::Windows::Forms::TextBox());
				this->function = (gcnew System::Windows::Forms::Label());
				this->variable2 = (gcnew System::Windows::Forms::TextBox());
				this->addition = (gcnew System::Windows::Forms::Button());
				this->subtraction = (gcnew System::Windows::Forms::Button());
				this->multiply = (gcnew System::Windows::Forms::Button());
				this->division = (gcnew System::Windows::Forms::Button());
				this->result = (gcnew System::Windows::Forms::Label());
				this->total = (gcnew System::Windows::Forms::Label());
				this->SuspendLayout();
				// 
				// variable1
				// 
				this->variable1->Font = (gcnew System::Drawing::Font(L"Microsoft Sans Serif", 28.25F));
				this->variable1->Location = System::Drawing::Point(102, 29);
				this->variable1->Name = L"variable1";
				this->variable1->Size = System::Drawing::Size(182, 50);
				this->variable1->TabIndex = 0;
				this->variable1->TextChanged += gcnew System::EventHandler(this, &MyForm::textBox1_TextChanged);
				// 
				// function
				// 
				this->function->AutoSize = true;
				this->function->Font = (gcnew System::Drawing::Font(L"Microsoft Sans Serif", 28.25F));
				this->function->ForeColor = System::Drawing::SystemColors::ControlText;
				this->function->Location = System::Drawing::Point(24, 93);
				this->function->Name = L"function";
				this->function->Size = System::Drawing::Size(0, 44);
				this->function->TabIndex = 1;
				this->function->Click += gcnew System::EventHandler(this, &MyForm::label1_Click);
				// 
				// variable2
				// 
				this->variable2->Font = (gcnew System::Drawing::Font(L"Microsoft Sans Serif", 28.25F));
				this->variable2->Location = System::Drawing::Point(102, 87);
				this->variable2->Name = L"variable2";
				this->variable2->Size = System::Drawing::Size(182, 50);
				this->variable2->TabIndex = 2;
				// 
				// addition
				// 
				this->addition->Font = (gcnew System::Drawing::Font(L"Microsoft Sans Serif", 28.25F));
				this->addition->Location = System::Drawing::Point(11, 270);
				this->addition->Name = L"addition";
				this->addition->Size = System::Drawing::Size(66, 61);
				this->addition->TabIndex = 3;
				this->addition->Text = L"+";
				this->addition->UseVisualStyleBackColor = true;
				this->addition->Click += gcnew System::EventHandler(this, &MyForm::addition_Click);
				// 
				// subtraction
				// 
				this->subtraction->Font = (gcnew System::Drawing::Font(L"Microsoft Sans Serif", 28.25F));
				this->subtraction->Location = System::Drawing::Point(83, 270);
				this->subtraction->Name = L"subtraction";
				this->subtraction->Size = System::Drawing::Size(63, 61);
				this->subtraction->TabIndex = 4;
				this->subtraction->Text = L"-";
				this->subtraction->UseVisualStyleBackColor = true;
				this->subtraction->Click += gcnew System::EventHandler(this, &MyForm::subtraction_Click);
				// 
				// multiply
				// 
				this->multiply->Font = (gcnew System::Drawing::Font(L"Microsoft Sans Serif", 28.25F));
				this->multiply->Location = System::Drawing::Point(152, 270);
				this->multiply->Name = L"multiply";
				this->multiply->Size = System::Drawing::Size(63, 61);
				this->multiply->TabIndex = 5;
				this->multiply->Text = L"*";
				this->multiply->UseVisualStyleBackColor = true;
				this->multiply->Click += gcnew System::EventHandler(this, &MyForm::multiply_Click);
				// 
				// division
				// 
				this->division->Font = (gcnew System::Drawing::Font(L"Microsoft Sans Serif", 28.25F));
				this->division->ImageAlign = System::Drawing::ContentAlignment::MiddleRight;
				this->division->Location = System::Drawing::Point(221, 270);
				this->division->Name = L"division";
				this->division->Size = System::Drawing::Size(63, 61);
				this->division->TabIndex = 6;
				this->division->Text = L"/";
				this->division->UseVisualStyleBackColor = true;
				this->division->Click += gcnew System::EventHandler(this, &MyForm::division_Click);
				// 
				// result
				// 
				this->result->AutoSize = true;
				this->result->Font = (gcnew System::Drawing::Font(L"Microsoft Sans Serif", 28.25F));
				this->result->Location = System::Drawing::Point(36, 174);
				this->result->Name = L"result";
				this->result->Size = System::Drawing::Size(41, 44);
				this->result->TabIndex = 7;
				this->result->Text = L"=";
				// 
				// total
				// 
				this->total->AutoSize = true;
				this->total->Font = (gcnew System::Drawing::Font(L"Microsoft Sans Serif", 28.25F));
				this->total->Location = System::Drawing::Point(96, 174);
				this->total->Name = L"total";
				this->total->Size = System::Drawing::Size(0, 44);
				this->total->TabIndex = 8;
				// 
				// MyForm
				// 
				this->AutoScaleDimensions = System::Drawing::SizeF(6, 13);
				this->AutoScaleMode = System::Windows::Forms::AutoScaleMode::Font;
				this->ClientSize = System::Drawing::Size(297, 336);
				this->Controls->Add(this->total);
				this->Controls->Add(this->result);
				this->Controls->Add(this->division);
				this->Controls->Add(this->multiply);
				this->Controls->Add(this->subtraction);
				this->Controls->Add(this->addition);
				this->Controls->Add(this->variable2);
				this->Controls->Add(this->function);
				this->Controls->Add(this->variable1);
				this->Name = L"MyForm";
				this->Text = L"MyForm";
				this->ResumeLayout(false);
				this->PerformLayout();

			}
  
  #Add fuctions to labels and textbox:
    
    #pragma endregion
	private: System::Void textBox1_TextChanged(System::Object^ sender, System::EventArgs^ e) {
	}
	private: System::Void label1_Click(System::Object^ sender, System::EventArgs^ e) {
	}
  
  #Convert strings enter into textbox into doubles and added functions to each respected button.
  
	private: System::Void addition_Click(System::Object^ sender, System::EventArgs^ e) {

		function->Text = "+";
		double result = System::Convert::ToDouble(variable1->Text)+ System::Convert::ToDouble(variable2->Text);
		 total->Text= System::Convert::ToString(result);

	}
      private: System::Void subtraction_Click(System::Object^ sender, System::EventArgs^ e) {

        function->Text = "-";
        double result = System::Convert::ToDouble(variable1->Text) - System::Convert::ToDouble(variable2->Text);
        total->Text = System::Convert::ToString(result);

    }
     private: System::Void multiply_Click(System::Object^ sender, System::EventArgs^ e) {

        function->Text = "*";
        double result = System::Convert::ToDouble(variable1->Text) * System::Convert::ToDouble(variable2->Text);
        total->Text = System::Convert::ToString(result);


    }
      private: System::Void division_Click(System::Object^ sender, System::EventArgs^ e) {

        function->Text = "/";
        double result = System::Convert::ToDouble(variable1->Text) / System::Convert::ToDouble(variable2->Text);
        total->Text = System::Convert::ToString(result);
    }
    };
    }

#RESULTS:
#![image](https://user-images.githubusercontent.com/127352211/223858545-de3e2bde-4da3-402a-aa84-5c830713af35.png) // ![image](https://user-images.githubusercontent.com/127352211/223858623-a8398b90-591c-48ed-889f-080b68fa292a.png) // ![image](https://user-images.githubusercontent.com/127352211/223858716-667a928b-427d-4e90-86d8-bc6989c24025.png) //![image](https://user-images.githubusercontent.com/127352211/223858806-93213c3e-19b6-4938-bbeb-fbb2753c2fa0.png)




