---
UID: NF:mfidl.MFCreateMediaSession
title: MFCreateMediaSession function
author: windows-sdk-content
description: Creates the Media Session in the application's process.
old-location: mf\mfcreatemediasession.htm
tech.root: MedFound
ms.assetid: 86b2b5ec-231c-4943-9add-1a5a60e72268
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 86b2b5ec-231c-4943-9add-1a5a60e72268, MFCreateMediaSession, MFCreateMediaSession function [Media Foundation], mf.mfcreatemediasession, mfidl/MFCreateMediaSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateMediaSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateMediaSession function


## -description



Creates the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> in the application's process.




## -parameters




### -param pConfiguration

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. This parameter can be <b>NULL</b>. See Remarks.
          


### -param ppMediaSession

Receives a pointer to the Media Session's <a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a> interface. The caller must release the interface. Before releasing the last reference to the <b>IMFMediaSession</b> pointer, the application must call the <a href="https://msdn.microsoft.com/5b9663c2-e32e-4075-b397-59ae01558e15">IMFMediaSession::Shutdown</a> method.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.
              

</td>
</tr>
</table>
 




## -remarks



If your application does not play protected content, you can use this function to create the Media Session in the application's process. To use the Media Session for protected content, you must call <a href="https://msdn.microsoft.com/cb492e68-3d8a-49b2-8c0b-bee8065b53a8">MFCreatePMPMediaSession</a>.
      

You can use the <i>pConfiguration</i> parameter to specify any of the following attributes:
      
        

<ul>
<li>
<a href="https://msdn.microsoft.com/6810a22c-f091-423c-97dd-c04fdabdb9bb">MF_SESSION_GLOBAL_TIME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a">MF_SESSION_QUALITY_MANAGER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/672274fb-71fc-49ca-bab6-1fc4de21d17c">MF_SESSION_TOPOLOADER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4D11B4D6-8CFF-4850-BF8F-9019A1F79153">MF_LOW_LATENCY</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/09f50b11-0e0a-42b6-a7bf-bb0135343351">About the Media Session</a>



<a href="https://msdn.microsoft.com/cb492e68-3d8a-49b2-8c0b-bee8065b53a8">MFCreatePMPMediaSession</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a>
 

 

