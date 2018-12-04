---
UID: NF:msctf.TF_GetThreadMgr
title: TF_GetThreadMgr function
author: windows-sdk-content
description: The TF_GetThreadMgr function obtains a copy of a thread manager object previously created within the calling thread.
old-location: tsf\tf_getthreadmgr.htm
tech.root: TSF
ms.assetid: f8e3ed16-7a4f-424a-ae6d-4f81ab344af0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: TF_GetThreadMgr, TF_GetThreadMgr function [Text Services Framework], msctf/TF_GetThreadMgr, tsf.tf_getthreadmgr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - msctf.dll
api_name:
 - TF_GetThreadMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows XPWindows 2000 Professional
---

# TF_GetThreadMgr function


## -description


The <b>TF_GetThreadMgr</b> function obtains a copy of a thread manager object previously created within the calling thread.


## -parameters




### -param pptim [out]

Pointer to an <a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a> interface pointer that receives the thread manager object. This receives <b>NULL</b> if no thread manager is created within the calling thread.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>The function was successful. <i>pptim</i> will be <b>NULL</b> if no thread manager is created within the calling thread.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -remarks



If no thread manager is created within the calling thread, this function will set <i>pptim</i> to <b>NULL</b> and return S_OK. Therefore, it is necessary to verify that the function succeeded and that <i>pptim</i> is not <b>NULL</b> before using <i>pptim</i>.


#### Examples

There is no import library available that defines this function, so it is necessary to manually obtain a pointer to this function using <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. The following code example demonstrates how to accomplish this.

The following example demonstrates a function that will attempt to obtain a copy of a previously created thread manager object. If no thread manager object exists within the calling thread, the function will create one.

<div class="alert"><b>Note</b>  <p class="note">Using <b>LoadLibrary</b> incorrectly can compromise the security of your application by loading the wrong DLL. Refer to the <b>LoadLibrary</b> documentation for information on how to correctly load DLLs with different versions of Windows.

</div>
<div> </div>
<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
typedef HRESULT (WINAPI *PTF_GETTHREADMGR)(ITfThreadMgr **pptim);

HRESULT GetThreadMgr(ITfThreadMgr **pptm)
{
    HRESULT hr = E_FAIL;
    HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));
    ITfThreadMgr *pThreadMgr = NULL;

    if(hMSCTF == NULL)
    {
        //Error loading module -- fail as securely as possible 
    }

    else
    {
        PTF_GETTHREADMGR pfnGetThreadMgr;
    
        pfnGetThreadMgr = (PTF_GETTHREADMGR)GetProcAddress(hMSCTF, "TF_GetThreadMgr");

        if(pfnGetThreadMgr)
        {
            hr = (*pfnGetThreadMgr)(&amp;pThreadMgr);
        }
        
        FreeLibrary(hMSCTF);
    }

    //If no object could be obtained, try to create one. 
    if(NULL == pThreadMgr)
    {
        //CoInitialize or OleInitialize must already have been called. 
        hr = CoCreateInstance(  CLSID_TF_ThreadMgr, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_ITfThreadMgr, 
                                (void**)&amp;pThreadMgr);
    }

    *pptm = pThreadMgr;

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr
      </a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>
 

 

