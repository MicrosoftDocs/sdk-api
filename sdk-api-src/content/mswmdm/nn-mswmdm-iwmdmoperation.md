---
UID: NN:mswmdm.IWMDMOperation
title: IWMDMOperation (mswmdm.h)
author: windows-sdk-content
description: This optional, application-implemented IWMDMOperation interface allows the application to control how data is read from or written to the computer during a file transfer.
old-location: wmdm\iwmdmoperation.htm
tech.root: WMDM
ms.assetid: 7277a8fe-3006-4456-b2e7-6041d3324f35
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMOperation, IWMDMOperation interface [windows Media Device Manager], IWMDMOperation interface [windows Media Device Manager],described, IWMDMOperationInterface, mswmdm/IWMDMOperation, wmdm.iwmdmoperation
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
ms.custom: 19H1
---

# IWMDMOperation interface


## -description



This optional, application-implemented <b>IWMDMOperation</b> interface allows the application to control how data is read from or written to the computer during a file transfer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMOperation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMOperation</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread">BeginRead</a>
</td>
<td align="left" width="63%">
Indicates that a "read from device" action is beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite">BeginWrite</a>
</td>
<td align="left" width="63%">
Indicates that a "write to device" action is beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end">End</a>
</td>
<td align="left" width="63%">
Indicates that a read or write operation is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes">GetObjectAttributes</a>
</td>
<td align="left" width="63%">
Allows the application to specify attributes for an object being written to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname">GetObjectName</a>
</td>
<td align="left" width="63%">
Allows the application to specify the name of an object being written to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize">GetObjectTotalSize</a>
</td>
<td align="left" width="63%">
Retrieves the total size of an object, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes">SetObjectAttributes</a>
</td>
<td align="left" width="63%">
Assigns the content attributes. This method is currently not called by Windows Media Device Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectname">SetObjectName</a>
</td>
<td align="left" width="63%">
Assigns a name to the content being read or written. This method is currently not called by Windows Media Device Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjecttotalsize">SetObjectTotalSize</a>
</td>
<td align="left" width="63%">
Assigns the total size of an object, in bytes. This method is currently not called by Windows Media Device Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">TransferObjectData</a>
</td>
<td align="left" width="63%">
Transfers a block of data to or from the computer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2">IWMDMOperation2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3">IWMDMOperation3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

