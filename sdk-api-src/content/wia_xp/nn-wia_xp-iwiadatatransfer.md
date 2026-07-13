---
UID: NN:wia_xp.IWiaDataTransfer
title: IWiaDataTransfer (wia_xp.h)
description: The IWiaDataTransfer interface is a high performance data transfer interface.
helpviewer_keywords: ["IWiaDataTransfer","IWiaDataTransfer interface [WIA]","IWiaDataTransfer interface [WIA]","described","_wia_IWiaDataTransfer","wia._wia_IWiaDataTransfer","wia_xp/IWiaDataTransfer"]
old-location: wia\_wia_IWiaDataTransfer.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatatransfer\iwiadatatransfer.htm
ms.date: 12/05/2018
ms.keywords: IWiaDataTransfer, IWiaDataTransfer interface [WIA], IWiaDataTransfer interface [WIA],described, _wia_IWiaDataTransfer, wia._wia_IWiaDataTransfer, wia_xp/IWiaDataTransfer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaDataTransfer
 - wia_xp/IWiaDataTransfer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDataTransfer
archived: true
---

# IWiaDataTransfer interface


## -description

The <b>IWiaDataTransfer</b> interface is a high performance data transfer interface. This interface supports a shared memory window to transfer data from the device object to the application, and eliminates unnecessary data copies during marshalling. A callback mechanism is provided in the form of the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback">IWiaDataCallback</a> interface. It enables applications to obtain data transfer status notification, transfer data from the Windows Image Acquisition (WIA) device to the application, and cancel pending data transfers. 
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="/windows/desktop/wia/-wia-iwiatransfer">IWiaTransfer</a> instead of <b>IWiaDataTransfer</b>.</div><div> </div>

## -inheritance

The <b>IWiaDataTransfer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaDataTransfer</b> also has these types of members:

## -remarks

The <b>IWiaDataTransfer</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
