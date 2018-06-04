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

# ICertView::OpenConnection


## -description


The <b>OpenConnection</b> method establishes a connection with a Certificate Services server.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the Certificate Services server. The configuration string is in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the server's network name, and CANAME is the common name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Upon successful completion of this method, the 
<a href="https://msdn.microsoft.com/0b6660ee-458f-457f-8a38-0d950aee2710">ICertView</a> object will have a connection to the Certificate Services server specified in the  <i>strConfig</i> parameter.

 To close the connection, call the <b>Release</b> function.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ICertView *   pCertView = NULL;
BSTR          strCertServ = NULL;
HRESULT       hr;

// Initialize COM.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

if (FAILED(hr))
{
    printf("Failed CoInitializeEx\n");
    goto error;
}
// Get pointer to the ICertView interface.
hr = CoCreateInstance(CLSID_CCertView,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_ICertView,
                      (void **)&amp;pCertView);
if (FAILED(hr))
{
    printf("Failed CoCreateInstance\n");
    goto error;
}
// The use of '\\' is necessary to represent a single backslash.
strCertServ = SysAllocString(TEXT("Server01\\ABCCertServ"));
// Open the connection to the Certificate Services server.
hr = pCertView-&gt;OpenConnection(strCertServ);
if (FAILED(hr))
{
    printf("Failed OpenConnection!\n");
    goto error;
}
else
    // Established successful connection; use view as appropriate.
    // ...
    // Done using objects; free resources.
error: 
    if (NULL != pCertView)
        pCertView-&gt;Release();
    if (NULL != strCertServ)
        SysFreeString(strCertServ);
    // Free COM resources.
    CoUninitialize();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>



<a href="https://msdn.microsoft.com/0b6660ee-458f-457f-8a38-0d950aee2710">ICertView</a>



<a href="https://msdn.microsoft.com/c29f1db3-0cdf-463e-a202-47fbba8e1c81">ICertView2</a>



<a href="https://msdn.microsoft.com/d68a5463-f711-4737-b0ad-889f7e4855d5">ICertView::OpenView</a>
 

 

