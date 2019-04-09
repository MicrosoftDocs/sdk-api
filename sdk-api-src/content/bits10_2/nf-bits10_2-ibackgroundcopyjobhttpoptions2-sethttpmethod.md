---
UID: NF:bits10_2.IBackgroundCopyJobHttpOptions2.SetHttpMethod
title: IBackgroundCopyJobHttpOptions2::SetHttpMethod (bits10_2.h)
author: windows-sdk-content
description: Overrides the default HTTP method used for a BITS transfer.
old-location: bits\ibackgroundcopyjobhttpoptions2_sethttpmethod.htm
tech.root: Bits
ms.assetid: 0CF8236B-7630-4A38-8A8F-51E69D3461B0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJobHttpOptions2 interface [BITS],SetHttpMethod method, IBackgroundCopyJobHttpOptions2.SetHttpMethod, IBackgroundCopyJobHttpOptions2::SetHttpMethod, SetHttpMethod, SetHttpMethod method [BITS], SetHttpMethod method [BITS],IBackgroundCopyJobHttpOptions2 interface, bits.ibackgroundcopyjobhttpoptions2_sethttpmethod, bits10_2/IBackgroundCopyJobHttpOptions2::SetHttpMethod
ms.topic: method
req.header: bits10_2.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits10_2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJobHttpOptions2.SetHttpMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJobHttpOptions2::SetHttpMethod


## -description


Overrides the default HTTP method used for a BITS transfer.


## -parameters




### -param method [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

A pointer to a constant null-terminated string of wide characters containing the HTTP method name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



BITS allows you, as the developer, to choose an HTTP method other than the default method. This increases BITS' ability to interact with servers that don't adhere to the normal BITS requirements for HTTP servers. Bear the following in mind when you choose a different HTTP method from the default one.

<ul>
<li>BITS automatically changes the job priority to <a href="https://msdn.microsoft.com/bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e">BG_JOB_PRIORITY_FOREGROUND</a>, and prevents that priority from being changed.</li>
<li>An error that would ordinarily  be resumable (such as loss of connectivity) transitions the job to an ERROR state. You, as the developer, can restart the job by calling <a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a>, and the job will be restarted from the beginning. See <a href="https://msdn.microsoft.com/b765a8ef-74bd-475e-9cd9-e9e2cf4f0305">Life Cycle of a BITS Job</a> for more information on BITS job states.</li>
<li>BITS doesn’t allow DYNAMIC_CONTENT nor ON_DEMAND_MODE jobs with <b>SetHttpMethod</b>.</li>
</ul>
<b>SetHttpMethod</b> does nothing if the method name that you pass matches the default HTTP method for the transfer type. For example, if you set a download job method to "GET" (the default), then the job priority won't be changed. The HTTP method must be set before the first call to <a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a> that starts the job.




## -see-also




<a href="https://msdn.microsoft.com/6E8A32CF-99F6-4C4D-A6EE-A05A1E601793">IBackgroundCopyJobHttpOptions2</a>
 

 

