---
UID: NF:contentpartner.IWMPContentContainerList.GetContainer
title: IWMPContentContainerList::GetContainer
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetContainer method retrieves the content container at the specified index.
old-location: wmp\iwmpcontentcontainerlist_getcontainer.htm
tech.root: WMP
ms.assetid: 8922aeed-0598-4dc8-86ac-e113697fcea9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetContainer, GetContainer method [Windows Media Player], GetContainer method [Windows Media Player],IWMPContentContainerList interface, IWMPContentContainerList interface [Windows Media Player],GetContainer method, IWMPContentContainerList.GetContainer, IWMPContentContainerList::GetContainer, IWMPContentContainerListGetContainer, contentpartner/IWMPContentContainerList::GetContainer, wmp.iwmpcontentcontainerlist_getcontainer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentContainerList.GetContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- contentpartner.h
: 
- IWMPContentContainerList.GetContainer
: 
---

# IWMPContentContainerList::GetContainer


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetContainer</b> method retrieves the content container at the specified index.




## -parameters




### -param idxContainer [in]

Specifies the index of the content container to retrieve.


### -param ppContent [out]

Address of a variable that receives a pointer to the <b>IWMPContentContainer</b> interface at the specified index.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd563130(v=VS.85).aspx">IWMPContentContainer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563131(v=VS.85).aspx">IWMPContentContainerList Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563133(v=VS.85).aspx">IWMPContentContainerList::GetContainerCount</a>
 

 

