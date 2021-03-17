---
UID: NF:fsrm.IFsrmSetting.EmailTest
title: IFsrmSetting::EmailTest (fsrm.h)
description: Send an email message to the specified email address.
helpviewer_keywords: ["EmailTest","EmailTest method [File Server Resource Manager]","EmailTest method [File Server Resource Manager]","FsrmSetting class","EmailTest method [File Server Resource Manager]","IFsrmSetting interface","FsrmSetting class [File Server Resource Manager]","EmailTest method","IFsrmSetting interface [File Server Resource Manager]","EmailTest method","IFsrmSetting.EmailTest","IFsrmSetting::EmailTest","fs.ifsrmsetting_emailtest","fsrm.ifsrmsetting_emailtest","fsrm/IFsrmSetting::EmailTest"]
old-location: fsrm\ifsrmsetting_emailtest.htm
tech.root: fsrm
ms.assetid: dda57309-8e77-4934-bb3e-d208d4607ea5
ms.date: 12/05/2018
ms.keywords: EmailTest, EmailTest method [File Server Resource Manager], EmailTest method [File Server Resource Manager],FsrmSetting class, EmailTest method [File Server Resource Manager],IFsrmSetting interface, FsrmSetting class [File Server Resource Manager],EmailTest method, IFsrmSetting interface [File Server Resource Manager],EmailTest method, IFsrmSetting.EmailTest, IFsrmSetting::EmailTest, fs.ifsrmsetting_emailtest, fsrm.ifsrmsetting_emailtest, fsrm/IFsrmSetting::EmailTest
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmSetting::EmailTest
 - fsrm/IFsrmSetting::EmailTest
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
 - IFsrmSetting.EmailTest
 - FsrmSetting.EmailTest
---

# IFsrmSetting::EmailTest


## -description

Send an email message to the specified email address.

## -parameters

### -param mailTo [in]

The email address. The string is limited to 255 characters.

## -returns

The method returns the following return codes:

## -remarks

Use this method to test the SMTP server specified in the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_smtpserver">SmtpServer</a> property. The sender is specified in 
    the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-get_mailfrom">MailFrom</a> property (cannot be set to 
    "[Admin Email]").

The subject and message body are predefined, localized text.


#### Examples

The following example shows how to call this method.


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
// Call the IFsrmSetting::EmailTest method to test the SMTP email server.
//
void wmain(void)
{
  HRESULT hr = 0;
  IFsrmSetting* pSettings = NULL;

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

  // Specify the SMTP server to use for sending email.
  hr = pSettings->put_SmtpServer(_bstr_t(L"<FQDNOFSMTPSERVER>")); 
  if (FAILED(hr))
  {
    wprintf(L"pSettings->put_SmtpServer failed, 0x%x.\n", hr);
    goto cleanup;
  }

  // Test the specified SMTP server. If the test succeeds, you will find a 
  // predefined email message in C:\Inetpub\mailroot\Drop. You can use 
  // Outlook Express to read the message.

  hr = pSettings->EmailTest(_bstr_t(L"admin@<FQDNOFSMTPSERVER>"));
  if (FAILED(hr))
  {
    wprintf(L"pSettings->EmailTest failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"Successfully sent mail.\n");

cleanup:

  if (pSettings)
    pSettings->Release();

  CoUninitialize();
}

```

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmsetting">FsrmSetting</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmsetting">IFsrmSetting</a>