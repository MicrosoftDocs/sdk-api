---
UID: NF:mfidl.MFCreatePMPMediaSession
title: MFCreatePMPMediaSession function
author: windows-driver-content
description: Creates an instance of the Media Session inside a Protected Media Path (PMP) process.
old-location: mf\mfcreatepmpmediasession.htm
old-project: medfound
ms.assetid: cb492e68-3d8a-49b2-8c0b-bee8065b53a8
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: MFCreatePMPMediaSession, MFCreatePMPMediaSession function [Media Foundation], cb492e68-3d8a-49b2-8c0b-bee8065b53a8, mf.mfcreatepmpmediasession, mfidl/MFCreatePMPMediaSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreatePMPMediaSession
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreatePMPMediaSession function


## -description



          Creates an instance of the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> inside a Protected Media Path (PMP) process.
        


## -parameters




### -param dwCreationFlags


            A member of the <a href="https://msdn.microsoft.com/6341aaff-aa80-4172-8577-0b757a01ea53">MFPMPSESSION_CREATION_FLAGS</a> enumeration that specifies how to create the session object.
          


### -param pConfiguration


            A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. This parameter can be <b>NULL</b>. See Remarks.
          


### -param ppMediaSession


            Receives a pointer to the PMP Media Session's <a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a> interface. The caller must release the interface. Before releasing the last reference to the <b>IMFMediaSession</b> pointer, the application must call the <a href="https://msdn.microsoft.com/5b9663c2-e32e-4075-b397-59ae01558e15">IMFMediaSession::Shutdown</a> method.
          


### -param ppEnablerActivate


            Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface or the value <b>NULL</b>. If non-<b>NULL</b>, the caller must release the interface. See Remarks.
          


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



You can use the <i>pConfiguration</i> parameter to set any of the following attributes:

<ul>
<li>
<a href="https://msdn.microsoft.com/66482541-63d4-439b-862f-7507605af5d8">MF_SESSION_CONTENT_PROTECTION_MANAGER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6810a22c-f091-423c-97dd-c04fdabdb9bb">MF_SESSION_GLOBAL_TIME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a">MF_SESSION_QUALITY_MANAGER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3a2f9ff5-1780-40f3-b36b-3a7cccb47d05">MF_SESSION_REMOTE_SOURCE_MODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a922c79b-d6c1-447d-b6fa-993970169a3f">MF_SESSION_SERVER_CONTEXT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/672274fb-71fc-49ca-bab6-1fc4de21d17c">MF_SESSION_TOPOLOADER</a>
</li>
</ul>
If this function cannot create the PMP Media Session because a trusted binary was revoked, the <i>ppEnablerActivate</i> parameter receives an <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface pointer. The application can use this pointer to create a content enabler object, which can then be used to download an updated binary:

<ol>
<li>
            Call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> with the interface identifier IID_IMFContentEnabler to get an <a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a> interface pointer.
          </li>
<li>
            Use that interface to download the updated binary.
          </li>
<li>
            Call <b>MFCreatePMPMediaSession</b> again.
          </li>
</ol>
If the function successfully creates the PMP Media Session, the <i>ppEnablerActivate</i> parameter receives the value <b>NULL</b>.

Do not make calls to the PMP Media Session from a thread that is processing a window message sent from another thread. To test whether the current thread falls into this category, call <a href="winui._win32_InSendMessage">InSendMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/86b2b5ec-231c-4943-9add-1a5a60e72268">MFCreateMediaSession</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

