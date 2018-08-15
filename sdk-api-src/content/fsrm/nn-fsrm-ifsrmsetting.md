---
UID: NN:fsrm.IFsrmSetting
title: IFsrmSetting
author: windows-sdk-content
description: Used to configure FSRM.
old-location: fsrm\ifsrmsetting.htm
old-project: fsrm
ms.assetid: 432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmSetting, IFsrmSetting interface [File Server Resource Manager], IFsrmSetting interface [File Server Resource Manager],described, fs.ifsrmsetting, fsrm.ifsrmsetting, fsrm/IFsrmSetting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, FsrmTlb.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmSetting
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmSetting interface


## -description


Used to configure FSRM.

To get this interface, call the 
    <a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmSetting</b> as the class identifier and 
    <code>__uuidof(IFsrmSetting)</code> as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmSetting</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFsrmSetting</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmSetting</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dda57309-8e77-4934-bb3e-d208d4607ea5">EmailTest</a>
</td>
<td align="left" width="63%">
Send a test email to the specified email address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbcd5532-4077-4a5c-94d4-e1fb636e6dda">GetActionRunLimitInterval</a>
</td>
<td align="left" width="63%">
Gets the time that an action that uses the global run limit interval must wait before the action is run 
     again.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cd4d583-2906-4ba0-b113-c21db143dec2">SetActionRunLimitInterval</a>
</td>
<td align="left" width="63%">
Sets the time that an action that uses the global run limit interval must wait before the action is run 
     again.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmSetting</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5985f697-f982-481c-896e-e6c3834f645d">AdminEmail</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the email address for the administrator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2c919dfd-86ba-4069-b8c9-caac27123429">DisableCommandLine</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets a value that determines whether FSRM prevents command line actions from running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6d185eca-6c14-4cd9-bb12-95499cde1050">EnableScreeningAudit</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets a value that determines whether FSRM keeps audit records of the file screen 
     violations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/62296c6c-d75b-4669-a665-a0c4321218b6">MailFrom</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the default email address from which email messages are sent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3d16e478-6e53-44d4-85ca-a4c508d138de">SmtpServer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the SMTP server that FSRM uses to send email.

</td>
</tr>
</table> 


## -remarks



To create this object from a script, use the program identifier, "Fsrm.FsrmSetting".


#### Examples

The following example shows how to retrieve the properties of this interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif


#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;comutil.h&gt;
#include &lt;fsrm.h&gt;       // FSRM base objects and collections
#include &lt;fsrmtlb_i.c&gt;  // contains CLSIDs


//
// Print the FSRM configuration settings.
//
void wmain(void)
{
  HRESULT hr = 0;
  IFsrmSetting* pSettings = NULL;
  BSTR bstr = NULL;
  VARIANT_BOOL boolVal = VARIANT_FALSE;
  long interval = 0;

  hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
  if (FAILED(hr))
  {
    wprintf(L"CoInitializeEx() failed, 0x%x.\n", hr);
    exit(1);
  }

  hr = CoCreateInstance(CLSID_FsrmSetting, 
                        NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IFsrmSetting),
                        reinterpret_cast&lt;void**&gt; (&amp;pSettings));

  if (FAILED(hr))
  {
    wprintf(L"CoCreateInstance(FsrmSetting) failed, 0x%x.\n", hr);
    if (E_ACCESSDENIED == hr)
      wprintf(L"Access denied. You must run the client with an elevated token.\n");

    goto cleanup;
  }

  wprintf(L"Successfully created Setting object.\n");

  // Get the default email address for the administrator. If set, you 
  // can then use the [Admin Email] macro for any action or report 
  // email address.
  hr = pSettings-&gt;get_AdminEmail(&amp;bstr);
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;get_AdminEmail failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"AdminEmail: %s\n", bstr);
  SysFreeString(bstr);

  // Determines whether FSRM allows command actions to execute. The default
  // is execute command actions.
  hr = pSettings-&gt;get_DisableCommandLine(&amp;boolVal);
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;get_DisableCommandLine failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"DisableCommandLine: %s\n", (VARIANT_TRUE == boolVal) ? L"True" : L"False");

  // Determines whether FSRM keeps audit records for file screen IO violations.
  // The default is not to keep audit records.
  hr = pSettings-&gt;get_EnableScreeningAudit(&amp;boolVal);
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;get_EnableScreeningAudit failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"EnableScreeningAudit: %s\n", (VARIANT_TRUE == boolVal) ? L"True" : L"False");

  // The default address from which reports and email actions are sent.
  // If set, you do not have to set the IFsrmActionEmail::MailFrom property.
  // The default is FSRM@&lt;localdomain&gt;
  hr = pSettings-&gt;get_MailFrom(&amp;bstr);
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;get_MailFrom failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"MailFrom: %s\n", bstr);
  SysFreeString(bstr);

  // Get the SMTP server. If not set, email is not sent.
  hr = pSettings-&gt;get_SmtpServer(&amp;bstr);
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;get_SmtpServer failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"SmtpServer: %s\n", bstr);
  SysFreeString(bstr);

  // Each action can specify an interval to wait before executing the action again.
  // The default for each action is 60 minutes.
  wprintf(L"Default interval, in minutes, to wait between executing an action:\n");

  hr = pSettings-&gt;GetActionRunLimitInterval(FsrmActionType_EventLog, &amp;interval);
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;GetActionRunLimitInterval(FsrmActionType_EventLog) failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"\tEventLog interval: %ld\n", interval);

  hr = pSettings-&gt;GetActionRunLimitInterval(FsrmActionType_Email, &amp;interval);
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;GetActionRunLimitInterval(FsrmActionType_Email) failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"\tEmail interval: %ld\n", interval);

  hr = pSettings-&gt;GetActionRunLimitInterval(FsrmActionType_Command, &amp;interval);
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;GetActionRunLimitInterval(FsrmActionType_Command) failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"\tCommand interval: %ld\n", interval);

  hr = pSettings-&gt;GetActionRunLimitInterval(FsrmActionType_Report, &amp;interval);
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;GetActionRunLimitInterval(FsrmActionType_Report) failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"\tReport interval: %ld\n", interval);

  hr = pSettings-&gt;put_SmtpServer(_bstr_t(L"&lt;FQDNOFSMTPSERVER&gt;"));
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;put_SmtpServer failed, 0x%x.\n", hr);
    goto cleanup;
  }

cleanup:

  if (pSettings)
    pSettings-&gt;Release();

  CoUninitialize();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/0c27393a-9a84-4147-a7e0-582c0bf2d918">FsrmSetting</a>
 

 

