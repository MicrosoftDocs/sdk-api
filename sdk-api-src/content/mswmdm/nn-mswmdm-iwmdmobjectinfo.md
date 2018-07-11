---
UID: NN:mswmdm.IWMDMObjectInfo
title: IWMDMObjectInfo
author: windows-sdk-content
description: The IWMDMObjectInfo interface gets and sets information that controls how playable files on device are handled by the IWMDMDeviceControl interface.This interface is not intended for non-playable files.
old-location: wmdm\iwmdmobjectinfo.htm
old-project: WMDM
ms.assetid: ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IWMDMObjectInfo, IWMDMObjectInfo interface [windows Media Device Manager], IWMDMObjectInfo interface [windows Media Device Manager],described, IWMDMObjectInfoInterface, mswmdm/IWMDMObjectInfo, wmdm.iwmdmobjectinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mswmdm.h
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMObjectInfo
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMObjectInfo interface


## -description



The <b>IWMDMObjectInfo</b> interface gets and sets information that controls how playable files on device are handled by the <a href="https://msdn.microsoft.com/e7b58957-4795-461f-ae3d-fb80e6711c9f">IWMDMDeviceControl</a> interface.

This interface is not intended for non-playable files. If the <b>IWMDMObjectInfo</b> interface is acquired from an <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface that represents a non-playable file, or a folder or a root file system containing no playable files, E_INVALIDTYPE is returned from all of the methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMObjectInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMObjectInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMObjectInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5b5cf7c-6969-497e-bf2c-e91ddb85f701">GetLastPlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the last play position of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81c7c30d-f217-4ea6-b785-bcccebd38d16">GetLongestPlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the longest play position of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f553513-0928-41b8-858f-c06ec57660d1">GetPlayLength</a>
</td>
<td align="left" width="63%">
Retrieves the play length of the object in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8642404a-33ff-40b7-b05a-f193e8feadf5">GetPlayOffset</a>
</td>
<td align="left" width="63%">
Retrieves the play offset of the object, in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca0e0efc-ff2e-40d6-ace3-5644013bccff">GetTotalLength</a>
</td>
<td align="left" width="63%">
Retrieves the total play length of the object in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dfa6443-4eb8-4a88-8af1-c082750e8d22">SetPlayLength</a>
</td>
<td align="left" width="63%">
Sets the play length of the object, in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b47cf5e8-1d5c-4a47-bb9a-0bec7203f497">SetPlayOffset</a>
</td>
<td align="left" width="63%">
Sets the play offset of the object, in units pertinent to the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

