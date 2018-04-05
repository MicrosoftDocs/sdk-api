---
UID: NF:oleauto.SetErrorInfo
title: SetErrorInfo function
author: windows-driver-content
description: Sets the error information object for the current logical thread of execution.
old-location: automat\seterrorinfo.htm
old-project: automat
ms.assetid: 8eaacfac-fc37-4eaa-870b-10b99d598d66
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SetErrorInfo, SetErrorInfo function [Automation], _oa96_SetErrorInfo, automat.seterrorinfo, oleauto/SetErrorInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
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
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
-	API-MS-Win-Downlevel-OLE32-l1-1-1.dll
-	ComBase.dll
api_name:
-	SetErrorInfo
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# SetErrorInfo function


## -description


Sets the error information object for the current logical thread of execution.


## -parameters




### -param dwReserved [in]

Reserved for future use. Must be zero.


### -param perrinfo [in, optional]

An error object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function releases the existing error information object, if one exists, and sets the pointer to <i>perrinfo</i>. Use this function after creating an error object that associates the object with the current logical thread of execution.

If the property or method that calls <b>SetErrorInfo</b> is called by <a href="https://msdn.microsoft.com/69b89e5c-2a04-4a6a-beb0-18e68f8866ac">DispInvoke</a>, then <b>DispInvoke</b> will fill the EXCEPINFO parameter with the values specified in the error information object. <b>DispInvoke</b> will return DISP_E_EXCEPTION when the property or method returns a failure return value for <b>DispInvoke</b>

Virtual function table (VTBL) binding controllers that do not use <a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">IDispatch::Invoke</a> can get the error information object by using <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>. This allows an object that supports a dual interface to use <b>SetErrorInfo</b>, regardless of whether the client uses VTBL binding or <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>.



When a cross apartment call is made COM clears out any error object.



Making a COM call that goes through a proxy-stub will clear any existing error object for the calling thread. A called object should not make any such calls after calling <b>SetErrorInfo</b> and before returning. The caller should not make any such calls after the call returns and before calling <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>. As a rule of thumb, an interface method should return as soon as possible after calling <b>SetErrorInfo</b>, and the caller should call <b>GetErrorInfo</b> as soon as possible after the call returns.



Entering the COM modal message loop will clear any existing error object. A called object should not enter a message loop after calling <b>SetErrorInfo</b>.



#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ICreateErrorInfo *pcerrinfo;
IErrorInfo *perrinfo;
HRESULT hr;

hr = CreateErrorInfo(&amp;pcerrinfo);
if (SUCCEEDED(hr))
{
   hr = pcerrinfo-&gt;QueryInterface(IID_IErrorInfo, (LPVOID FAR*) &amp;perrinfo);
   if (SUCCEEDED(hr))
   {
      SetErrorInfo(0, perrinfo);
      perrinfo-&gt;Release();
   }
   pcerrinfo-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>


