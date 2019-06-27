---
UID: NN:mswmdm.IMDSPObjectInfo
title: IMDSPObjectInfo (mswmdm.h)
author: windows-sdk-content
description: The IMDSPObjectInfo interface provides methods for getting and setting parameters that describe how playable objects on a storage medium are referenced or accessed by the IMDSPDeviceControl interface.
old-location: wmdm\imdspobjectinfo.htm
tech.root: WMDM
ms.assetid: f0003b14-7ae7-4822-befe-6bb1779328ec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPObjectInfo, IMDSPObjectInfo interface [windows Media Device Manager], IMDSPObjectInfo interface [windows Media Device Manager],described, IMDSPObjectInfoInterface, mswmdm/IMDSPObjectInfo, wmdm.imdspobjectinfo
ms.topic: interface
f1_keywords: 
 - "mswmdm/IMDSPObjectInfo"
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
 - IMDSPObjectInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPObjectInfo interface


## -description



The <b>IMDSPObjectInfo</b> interface provides methods for getting and setting parameters that describe how playable objects on a storage medium are referenced or accessed by the <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol">IMDSPDeviceControl</a> interface. Implementing this interface is optional. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

The resolution of the method parameters depends on the associated storage object as follows:

<ul>
<li>If the storage object represents a playable audio file, then the relative storage units are milliseconds.</li>
<li>If the storage object represents a folder or the root of a storage medium containing playable files, then the relative storage units are tracks.</li>
</ul>
This interface is not intended for non-playable files. If the <b>IMDSPObjectInfo</b> interface is acquired from an <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage</a> interface that represents a non-playable file or a folder or a root file system containing no playable files, E_INVALIDTYPE is returned from all of the methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPObjectInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPObjectInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPObjectInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-getlastplayposition">GetLastPlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the last play position of the object. The object must be a music file on the media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-getlongestplayposition">GetLongestPlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the longest play position of the object. The object must be a music file on the media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-getplaylength">GetPlayLength</a>
</td>
<td align="left" width="63%">
Retrieves the play length of the object in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-getplayoffset">GetPlayOffset</a>
</td>
<td align="left" width="63%">
Retrieves the play offset of the object, in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-gettotallength">GetTotalLength</a>
</td>
<td align="left" width="63%">
Retrieves the total play length of the object in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-setplaylength">SetPlayLength</a>
</td>
<td align="left" width="63%">
Sets the play length of the object, in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobjectinfo-setplayoffset">SetPlayOffset</a>
</td>
<td align="left" width="63%">
Sets the play offset of the object, in units pertinent to the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 

