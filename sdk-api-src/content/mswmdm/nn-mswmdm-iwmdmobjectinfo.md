---
UID: NN:mswmdm.IWMDMObjectInfo
title: IWMDMObjectInfo (mswmdm.h)
description: The IWMDMObjectInfo interface gets and sets information that controls how playable files on device are handled by the IWMDMDeviceControl interface.This interface is not intended for non-playable files.
helpviewer_keywords: ["IWMDMObjectInfo","IWMDMObjectInfo interface [windows Media Device Manager]","IWMDMObjectInfo interface [windows Media Device Manager]","described","IWMDMObjectInfoInterface","mswmdm/IWMDMObjectInfo","wmdm.iwmdmobjectinfo"]
old-location: wmdm\iwmdmobjectinfo.htm
tech.root: WMDM
ms.assetid: ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a
ms.date: 12/05/2018
ms.keywords: IWMDMObjectInfo, IWMDMObjectInfo interface [windows Media Device Manager], IWMDMObjectInfo interface [windows Media Device Manager],described, IWMDMObjectInfoInterface, mswmdm/IWMDMObjectInfo, wmdm.iwmdmobjectinfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMObjectInfo
 - mswmdm/IWMDMObjectInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMObjectInfo
---

# IWMDMObjectInfo interface


## -description

The <b>IWMDMObjectInfo</b> interface gets and sets information that controls how playable files on device are handled by the <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol">IWMDMDeviceControl</a> interface.

This interface is not intended for non-playable files. If the <b>IWMDMObjectInfo</b> interface is acquired from an <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage</a> interface that represents a non-playable file, or a folder or a root file system containing no playable files, E_INVALIDTYPE is returned from all of the methods.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMObjectInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMObjectInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-getlastplayposition">GetLastPlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the last play position of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-getlongestplayposition">GetLongestPlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the longest play position of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-getplaylength">GetPlayLength</a>
</td>
<td align="left" width="63%">
Retrieves the play length of the object in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-getplayoffset">GetPlayOffset</a>
</td>
<td align="left" width="63%">
Retrieves the play offset of the object, in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-gettotallength">GetTotalLength</a>
</td>
<td align="left" width="63%">
Retrieves the total play length of the object in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-setplaylength">SetPlayLength</a>
</td>
<td align="left" width="63%">
Sets the play length of the object, in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmobjectinfo-setplayoffset">SetPlayOffset</a>
</td>
<td align="left" width="63%">
Sets the play offset of the object, in units pertinent to the object.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>

