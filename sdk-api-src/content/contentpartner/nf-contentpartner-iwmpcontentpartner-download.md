---
UID: NF:contentpartner.IWMPContentPartner.Download
title: IWMPContentPartner::Download
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The Download method initiates the download of a set of media items.
old-location: wmp\iwmpcontentpartner_download.htm
old-project: WMP
ms.assetid: 0fa3ed40-e155-4e42-b031-d6cb8f8b4ac4
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Download, Download method [Windows Media Player], Download method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],Download method, IWMPContentPartner.Download, IWMPContentPartner::Download, IWMPContentPartnerDownload, contentpartner/IWMPContentPartner::Download, wmp.iwmpcontentpartner_download
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: contentpartner.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
tech.root: 
req.typenames: WMPTransactionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartner.Download
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartner::Download


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Download</b> method initiates the download of a set of media items.




## -parameters




### -param pInfo [in]

Pointer to an <a href="https://msdn.microsoft.com/a8fd239b-2a53-4db4-8a82-a7c510d215bc">IWMPContentContainerList</a> interface that describes the content to download.


### -param cookie [in]

A cookie that represents the download request.


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
</table>
 




## -remarks



This method initiates the process of inspecting the container list passed in <i>pInfo</i> and then returns immediately. As the plug-in inspects the container list, it calls <a href="https://msdn.microsoft.com/fe8772fa-2eb4-4dfe-b677-e667b6021690">IWMPContentPartnerCallback::DownloadTrack</a> once for each track in the container list. For more information about the download procedure, see <a href="https://msdn.microsoft.com/0a057e13-6e0c-4a8f-9cab-051183e6b222">Downloading Media Content</a>.




## -see-also




<a href="https://msdn.microsoft.com/a8fd239b-2a53-4db4-8a82-a7c510d215bc">IWMPContentContainerList Interface</a>



<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>



<a href="https://msdn.microsoft.com/9614e266-259c-411f-93cf-9be87c930b16">IWMPContentPartner::DownloadTrackComplete</a>
 

 

