---
UID: NN:mswmdm.IWMDMOperation
title: IWMDMOperation
author: windows-sdk-content
description: This optional, application-implemented IWMDMOperation interface allows the application to control how data is read from or written to the computer during a file transfer.
old-location: wmdm\iwmdmoperation.htm
tech.root: WMDM
ms.assetid: 7277a8fe-3006-4456-b2e7-6041d3324f35
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMDMOperation, IWMDMOperation interface [windows Media Device Manager], IWMDMOperation interface [windows Media Device Manager],described, IWMDMOperationInterface, mswmdm/IWMDMOperation, wmdm.iwmdmoperation
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMOperation interface


## -description



This optional, application-implemented <b>IWMDMOperation</b> interface allows the application to control how data is read from or written to the computer during a file transfer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMOperation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e72caaac-8992-4f11-8020-0455b3d730ad">BeginRead</a>
</td>
<td align="left" width="63%">
Indicates that a "read from device" action is beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b35b026-1fc1-44e8-befc-211d3387bc92">BeginWrite</a>
</td>
<td align="left" width="63%">
Indicates that a "write to device" action is beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1a3f0b7-033d-4e93-aaca-43db88a9b705">End</a>
</td>
<td align="left" width="63%">
Indicates that a read or write operation is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e1f4300-057d-40df-8e5c-75765f9ce337">GetObjectAttributes</a>
</td>
<td align="left" width="63%">
Allows the application to specify attributes for an object being written to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e66882ec-2fcf-44c7-b78a-a3b55d9e9ec4">GetObjectName</a>
</td>
<td align="left" width="63%">
Allows the application to specify the name of an object being written to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50ab01f9-0f38-485e-b7d9-98bc95948427">GetObjectTotalSize</a>
</td>
<td align="left" width="63%">
Retrieves the total size of an object, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ee2eabe-c20d-48fe-96f4-cb4143869462">SetObjectAttributes</a>
</td>
<td align="left" width="63%">
Assigns the content attributes. This method is currently not called by Windows Media Device Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d15b9cb0-6984-401e-9f81-97d0aae17b76">SetObjectName</a>
</td>
<td align="left" width="63%">
Assigns a name to the content being read or written. This method is currently not called by Windows Media Device Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/009716e8-6a4e-4373-9a7c-69dad815e743">SetObjectTotalSize</a>
</td>
<td align="left" width="63%">
Assigns the total size of an object, in bytes. This method is currently not called by Windows Media Device Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">TransferObjectData</a>
</td>
<td align="left" width="63%">
Transfers a block of data to or from the computer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/b3f7e92a-8feb-47cd-ae50-bc5bf9a37958">IWMDMOperation2 Interface</a>



<a href="https://msdn.microsoft.com/5ab4fdd2-d0bf-4e2c-b529-331ffa4c8403">IWMDMOperation3 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

