---
UID: NF:wmsdkidl.IWMDRMReader.Individualize
title: IWMDRMReader::Individualize
author: windows-sdk-content
description: The Individualize method individualizes the client by updating their DRM system components.
old-location: wmformat\iwmdrmreader_individualize.htm
old-project: wmformat
ms.assetid: 51bf9aa0-4c96-4c0b-8e5e-b63fd20dcc4d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMDRMReader interface [windows Media Format],Individualize method, IWMDRMReader.Individualize, IWMDRMReader::Individualize, IWMDRMReaderIndividualize, Individualize, Individualize method [windows Media Format], Individualize method [windows Media Format],IWMDRMReader interface, wmformat.iwmdrmreader_individualize, wmsdkidl/IWMDRMReader::Individualize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDRMReader.Individualize
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMReader::Individualize


## -description


<p class="CCE_Message">[<b>Individualize</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>Individualize</b> method individualizes the client by updating their DRM system components.




## -parameters




### -param dwFlags [in]

<b>DWORD</b> containing the relevant flags.

<table>
<tr>
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>0x0</td>
<td>Indicates that the client can be individualized again.</td>
</tr>
<tr>
<td>0x1</td>
<td>Indicates that the client will not be individualized again.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A null or invalid argument has been passed in.

</td>
</tr>
</table>
 




## -remarks



This is an asynchronous call that returns immediately. To abandon the attempt, call <b>CancelIndividualization</b>.

<div class="alert"><b>Important</b>  Because this operation will cause the user's system to be modified, you should display a message that explains what this operation will do and let the user choose whether or not to individualize. For more information and suggested message text, see <a href="https://msdn.microsoft.com/8f129bc1-3db9-4b41-9d60-daff037237ff">DRM Individualization</a>.</div>
<div> </div>
Individualization is the process of making the DRM client unique by downloading and installing an individualized component from the Microsoft Individualization Service. The entire process is performed automatically after an application calls the <b>Individualize</b> method. The application is informed of the progress of the individualization process through repeated <b>WMT_INDIVIDUALIZE</b> events, each of which has an associated <a href="https://msdn.microsoft.com/3779ed6f-c133-4a9d-b60c-ef8c41fcc4af">WM_INDIVIDUALIZE_STATUS</a> structure which is sent to the application's <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback method.

There are two times to initiate the individualization process: the first is when a piece of content requires it, and the second is when a player individualizes the client as part of the setup. In the latter case, there is no reason to individualize the client again.




## -see-also




<a href="https://msdn.microsoft.com/8f129bc1-3db9-4b41-9d60-daff037237ff">DRM Individualization</a>



<a href="https://msdn.microsoft.com/bf4ff0f3-1f78-43c4-be4d-c74209176e58">IWMDRMReader Interface</a>



<a href="https://msdn.microsoft.com/837d6fee-d5ba-49d8-ac69-e8ff010a787d">IWMDRMReader::CancelIndividualization</a>



<a href="https://msdn.microsoft.com/8d87c663-bc54-4928-9eee-d09c358e61f8">Individualizing DRM Applications</a>



<a href="https://msdn.microsoft.com/3779ed6f-c133-4a9d-b60c-ef8c41fcc4af">WM_INDIVIDUALIZE_STATUS</a>
 

 

