---
UID: NF:contentpartner.IWMPContentContainerList.GetContainerCount
title: IWMPContentContainerList::GetContainerCount
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetContainerCount method retrieves the count of content containers in the container list.
old-location: wmp\iwmpcontentcontainerlist_getcontainercount.htm
old-project: WMP
ms.assetid: e1ed4873-5d07-4a96-bd99-31ceeb423f98
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: GetContainerCount, GetContainerCount method [Windows Media Player], GetContainerCount method [Windows Media Player],IWMPContentContainerList interface, IWMPContentContainerList interface [Windows Media Player],GetContainerCount method, IWMPContentContainerList.GetContainerCount, IWMPContentContainerList::GetContainerCount, IWMPContentContainerListGetContainerCount, contentpartner/IWMPContentContainerList::GetContainerCount, wmp.iwmpcontentcontainerlist_getcontainercount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: contentpartner.h
req.include-header: 
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
 - IWMPContentContainerList.GetContainerCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentContainerList::GetContainerCount


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetContainerCount</b> method retrieves the count of content containers in the container list.




## -parameters




### -param pcContainer [out]

Address of a <b>ULONG</b> that receives the count.


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
 




## -see-also




<a href="https://msdn.microsoft.com/a8fd239b-2a53-4db4-8a82-a7c510d215bc">IWMPContentContainerList Interface</a>



<a href="https://msdn.microsoft.com/8922aeed-0598-4dc8-86ac-e113697fcea9">IWMPContentContainerList::GetContainer</a>
 

 

