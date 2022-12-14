---
UID: NN:fsrm.IFsrmSetting
title: IFsrmSetting (fsrm.h)
description: Used to configure FSRM.
helpviewer_keywords: ["IFsrmSetting","IFsrmSetting interface [File Server Resource Manager]","IFsrmSetting interface [File Server Resource Manager]","described","fs.ifsrmsetting","fsrm.ifsrmsetting","fsrm/IFsrmSetting"]
old-location: fsrm\ifsrmsetting.htm
tech.root: fsrm
ms.assetid: 432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b
ms.date: 12/05/2018
ms.keywords: IFsrmSetting, IFsrmSetting interface [File Server Resource Manager], IFsrmSetting interface [File Server Resource Manager],described, fs.ifsrmsetting, fsrm.ifsrmsetting, fsrm/IFsrmSetting
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmSetting
 - fsrm/IFsrmSetting
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmSetting
---

# IFsrmSetting interface


## -description

Used to configure FSRM.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmSetting</b> as the class identifier and 
    <code>__uuidof(IFsrmSetting)</code> as the interface identifier.

## -inheritance

The <b>IFsrmSetting</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmSetting</b> also has these types of members:

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

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmsetting">FsrmSetting</a>
