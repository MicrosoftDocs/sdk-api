---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
    <a href="https://msdn.microsoft.com/3d16e478-6e53-44d4-85ca-a4c508d138de">SmtpServer</a> property. The sender is specified in 
    the <a href="https://msdn.microsoft.com/62296c6c-d75b-4669-a665-a0c4321218b6">MailFrom</a> property (cannot be set to 
    "[Admin Email]").

The subject and message body are predefined, localized text.


#### Examples

The following example shows how to call this method.

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
                        reinterpret_cast&lt;void**&gt; (&amp;pSettings));

  if (FAILED(hr))
  {
    wprintf(L"CoCreateInstance(FsrmSetting) failed, 0x%x.\n", hr);
    if (E_ACCESSDENIED == hr)
      wprintf(L"Access denied. You must run the client with an elevated token.\n");

    goto cleanup;
  }

  wprintf(L"Successfully created Setting object.\n");

  // Specify the SMTP server to use for sending email.
  hr = pSettings-&gt;put_SmtpServer(_bstr_t(L"&lt;FQDNOFSMTPSERVER&gt;")); 
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;put_SmtpServer failed, 0x%x.\n", hr);
    goto cleanup;
  }

  // Test the specified SMTP server. If the test succeeds, you will find a 
  // predefined email message in C:\Inetpub\mailroot\Drop. You can use 
  // Outlook Express to read the message.

  hr = pSettings-&gt;EmailTest(_bstr_t(L"admin@&lt;FQDNOFSMTPSERVER&gt;"));
  if (FAILED(hr))
  {
    wprintf(L"pSettings-&gt;EmailTest failed, 0x%x.\n", hr);
    goto cleanup;
  }

  wprintf(L"Successfully sent mail.\n");

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




<a href="https://msdn.microsoft.com/0c27393a-9a84-4147-a7e0-582c0bf2d918">FsrmSetting</a>



<a href="https://msdn.microsoft.com/432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b">IFsrmSetting</a>
 

 

