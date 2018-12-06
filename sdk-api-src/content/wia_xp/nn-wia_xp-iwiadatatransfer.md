---
UID: NN:wia_xp.IWiaDataTransfer
title: IWiaDataTransfer
author: windows-sdk-content
description: The IWiaDataTransfer interface is a high performance data transfer interface.
old-location: wia\_wia_IWiaDataTransfer.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatatransfer\iwiadatatransfer.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWiaDataTransfer, IWiaDataTransfer interface [WIA], IWiaDataTransfer interface [WIA],described, _wia_IWiaDataTransfer, wia._wia_IWiaDataTransfer, wia_xp/IWiaDataTransfer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDataTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWiaDataTransfer interface


## -description


The <b>IWiaDataTransfer</b> interface is a high performance data transfer interface. This interface supports a shared memory window to transfer data from the device object to the application, and eliminates unnecessary data copies during marshalling. A callback mechanism is provided in the form of the <a href="https://msdn.microsoft.com/c2414d68-604f-4ae7-8808-7931240b1d26">IWiaDataCallback</a> interface. It enables applications to obtain data transfer status notification, transfer data from the Windows Image Acquisition (WIA) device to the application, and cancel pending data transfers. 
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://msdn.microsoft.com/7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0">IWiaTransfer</a> instead of <b>IWiaDataTransfer</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaDataTransfer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaDataTransfer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaDataTransfer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e4c6bf5-30b1-45a9-b815-b7cc45a6d387">idtEnumWIA_FORMAT_INFO</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2e4c6bf5-30b1-45a9-b815-b7cc45a6d387">IWiaDataTransfer::idtEnumWIA_FORMAT_INFO</a> method creates a banded transfer implementation of the <a href="https://msdn.microsoft.com/9f3e94bc-fa90-4e3d-97c5-17e57055de0e">IEnumWIA_FORMAT_INFO</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cbef4c0-cf28-4fdd-b347-84428ffd671b">idtGetBandedData</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3cbef4c0-cf28-4fdd-b347-84428ffd671b">IWiaDataTransfer::idtGetBandedData</a> method transfers a band of data from a hardware device to an application. For efficiency, applications retrieve data from WIA hardware devices in successive bands. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/595291d7-e81e-42f0-932a-f52895a822db">idtGetData</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/595291d7-e81e-42f0-932a-f52895a822db">IWiaDataTransfer::idtGetData</a> method retrieves complete files from a WIA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/268a5c3e-2717-40c3-9f24-cc490b1e593b">idtGetExtendedTransferInfo</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/268a5c3e-2717-40c3-9f24-cc490b1e593b">IWiaDataTransfer::idtGetExtendedTransferInfo</a> retrieves extended information relating to data transfer buffers in the case of banded data transfers. Applications typically use this method to retrieve driver recommended settings for minimum buffer size, maximum buffer size, and optimal buffer size for banded data transfers. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be2d8393-70c3-43a5-9455-7a0e9f48b5d6">idtQueryGetData</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/be2d8393-70c3-43a5-9455-7a0e9f48b5d6">IWiaDataTransfer::idtQueryGetData</a> method is used by applications to query a WIA device to determine what types of data formats it supports.


</td>
</tr>
</table> 


## -remarks



The <b>IWiaDataTransfer</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 



