---
UID: NN:fsrm.IFsrmSetting
title: IFsrmSetting (fsrm.h)
author: windows-sdk-content
description: Used to configure FSRM.
old-location: fsrm\ifsrmsetting.htm
tech.root: fsrm
ms.assetid: 432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmSetting, IFsrmSetting interface [File Server Resource Manager], IFsrmSetting interface [File Server Resource Manager],described, fs.ifsrmsetting, fsrm.ifsrmsetting, fsrm/IFsrmSetting
ms.topic: interface
f1_keywords: 
 - "fsrm/IFsrmSetting"
dev_langs:
 - c++
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, FsrmTlb.h
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
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmSetting
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmSetting interface


## -description


Used to configure FSRM.

To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmSetting</b> as the class identifier and 
    <code>__uuidof(IFsrmSetting)</code> as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmSetting</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmSetting</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-emailtest">EmailTest</a>
</td>
<td align="left" width="63%">
Send a test email to the specified email address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-getactionrunlimitinterval">GetActionRunLimitInterval</a>
</td>
<td align="left" width="63%">
Gets the time that an action that uses the global run limit interval must wait before the action is run 
     again.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-setactionrunlimitinterval">SetActionRunLimitInterval</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_adminemail">AdminEmail</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_disablecommandline">DisableCommandLine</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_enablescreeningaudit">EnableScreeningAudit</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_mailfrom">MailFrom</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_smtpserver">SmtpServer</a>


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


```cpp
#ifndef UNICODE
#define UNICODE
#endif


#include <windows.h>
#include <stdio.h>
#include <comutil.h>
#include <fsrm.h>       // FSRM base objects and collections
#include <fsrmtlb_i.c>  // contains CLSIDs


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
                        reinterpret_cast<void**> (&pSettings));

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
  hr = pSettings->get_AdminEmail(&bstr);
  if (FAILED(hr))
  {
    wprintf(L"pSettings->get_AdminEmail failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"AdminEmail: %s\n", bstr);
  SysFreeString(bstr);

  // Determines whether FSRM allows command actions to execute. The default
  // is execute command actions.
  hr = pSettings->get_DisableCommandLine(&boolVal);
  if (FAILED(hr))
  {
    wprintf(L"pSettings->get_DisableCommandLine failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"DisableCommandLine: %s\n", (VARIANT_TRUE == boolVal) ? L"True" : L"False");

  // Determines whether FSRM keeps audit records for file screen IO violations.
  // The default is not to keep audit records.
  hr = pSettings->get_EnableScreeningAudit(&boolVal);
  if (FAILED(hr))
  {
    wprintf(L"pSettings->get_EnableScreeningAudit failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"EnableScreeningAudit: %s\n", (VARIANT_TRUE == boolVal) ? L"True" : L"False");

  // The default address from which reports and email actions are sent.
  // If set, you do not have to set the IFsrmActionEmail::MailFrom property.
  // The default is FSRM@<localdomain>
  hr = pSettings->get_MailFrom(&bstr);
  if (FAILED(hr))
  {
    wprintf(L"pSettings->get_MailFrom failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"MailFrom: %s\n", bstr);
  SysFreeString(bstr);

  // Get the SMTP server. If not set, email is not sent.
  hr = pSettings->get_SmtpServer(&bstr);
  if (FAILED(hr))
  {
    wprintf(L"pSettings->get_SmtpServer failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"SmtpServer: %s\n", bstr);
  SysFreeString(bstr);

  // Each action can specify an interval to wait before executing the action again.
  // The default for each action is 60 minutes.
  wprintf(L"Default interval, in minutes, to wait between executing an action:\n");

  hr = pSettings->GetActionRunLimitInterval(FsrmActionType_EventLog, &interval);
  if (FAILED(hr))
  {
    wprintf(L"pSettings->GetActionRunLimitInterval(FsrmActionType_EventLog) failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"\tEventLog interval: %ld\n", interval);

  hr = pSettings->GetActionRunLimitInterval(FsrmActionType_Email, &interval);
  if (FAILED(hr))
  {
    wprintf(L"pSettings->GetActionRunLimitInterval(FsrmActionType_Email) failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"\tEmail interval: %ld\n", interval);

  hr = pSettings->GetActionRunLimitInterval(FsrmActionType_Command, &interval);
  if (FAILED(hr))
  {
    wprintf(L"pSettings->GetActionRunLimitInterval(FsrmActionType_Command) failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"\tCommand interval: %ld\n", interval);

  hr = pSettings->GetActionRunLimitInterval(FsrmActionType_Report, &interval);
  if (FAILED(hr))
  {
    wprintf(L"pSettings->GetActionRunLimitInterval(FsrmActionType_Report) failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"\tReport interval: %ld\n", interval);

  hr = pSettings->put_SmtpServer(_bstr_t(L"<FQDNOFSMTPSERVER>"));
  if (FAILED(hr))
  {
    wprintf(L"pSettings->put_SmtpServer failed, 0x%x.\n", hr);
    goto cleanup;
  }

cleanup:

  if (pSettings)
    pSettings->Release();

  CoUninitialize();
}

```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmsetting">FsrmSetting</a>
 

 

