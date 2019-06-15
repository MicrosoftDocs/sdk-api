---
UID: NN:wia_xp.IWiaDataTransfer
title: IWiaDataTransfer (wia_xp.h)
author: windows-sdk-content
description: The IWiaDataTransfer interface is a high performance data transfer interface.
old-location: wia\_wia_IWiaDataTransfer.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatatransfer\iwiadatatransfer.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWiaDataTransfer, IWiaDataTransfer interface [WIA], IWiaDataTransfer interface [WIA],described, _wia_IWiaDataTransfer, wia._wia_IWiaDataTransfer, wia_xp/IWiaDataTransfer
ms.topic: interface
f1_keywords: ["wia_xp/IWiaDataTransfer"]
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
ms.custom: 19H1
---

# IWiaDataTransfer interface


## -description


The <b>IWiaDataTransfer</b> interface is a high performance data transfer interface. This interface supports a shared memory window to transfer data from the device object to the application, and eliminates unnecessary data copies during marshalling. A callback mechanism is provided in the form of the <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback">IWiaDataCallback</a> interface. It enables applications to obtain data transfer status notification, transfer data from the Windows Image Acquisition (WIA) device to the application, and cancel pending data transfers. 
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://docs.microsoft.com/windows/desktop/wia/-wia-iwiatransfer">IWiaTransfer</a> instead of <b>IWiaDataTransfer</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaDataTransfer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaDataTransfer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info">idtEnumWIA_FORMAT_INFO</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info">IWiaDataTransfer::idtEnumWIA_FORMAT_INFO</a> method creates a banded transfer implementation of the <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info">IEnumWIA_FORMAT_INFO</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetbandeddata">idtGetBandedData</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetbandeddata">IWiaDataTransfer::idtGetBandedData</a> method transfers a band of data from a hardware device to an application. For efficiency, applications retrieve data from WIA hardware devices in successive bands. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata">idtGetData</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata">IWiaDataTransfer::idtGetData</a> method retrieves complete files from a WIA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetextendedtransferinfo">idtGetExtendedTransferInfo</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetextendedtransferinfo">IWiaDataTransfer::idtGetExtendedTransferInfo</a> retrieves extended information relating to data transfer buffers in the case of banded data transfers. Applications typically use this method to retrieve driver recommended settings for minimum buffer size, maximum buffer size, and optimal buffer size for banded data transfers. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtquerygetdata">idtQueryGetData</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtquerygetdata">IWiaDataTransfer::idtQueryGetData</a> method is used by applications to query a WIA device to determine what types of data formats it supports.


</td>
</tr>
</table> 


## -remarks



The <b>IWiaDataTransfer</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 



