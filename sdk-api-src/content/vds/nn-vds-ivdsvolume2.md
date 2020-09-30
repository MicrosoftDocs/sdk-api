---
UID: NN:vds.IVdsVolume2
title: IVdsVolume2 (vds.h)
description: Provides a method for returning volume property information, including the volume GUIDs.
helpviewer_keywords: ["IVdsVolume2","IVdsVolume2 interface","IVdsVolume2 interface","described","base.ivdsvolume2","vds/IVdsVolume2"]
old-location: base\ivdsvolume2.htm
tech.root: base
ms.assetid: 78077ce6-04f7-4d76-9057-40941feb941b
ms.date: 12/05/2018
ms.keywords: IVdsVolume2, IVdsVolume2 interface, IVdsVolume2 interface,described, base.ivdsvolume2, vds/IVdsVolume2
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsVolume2
 - vds/IVdsVolume2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVolume2
---

# IVdsVolume2 interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method for returning volume property information, including the volume GUIDs.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolume2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVolume2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolume2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vds/nf-vds-ivdsvolume2-getproperties2">GetProperties2</a>
</td>
<td align="left" width="63%">
Returns 
   property information for the current volume. This method is identical to the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-getproperties">IVdsVolume::GetProperties</a> method, except that it returns a <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop2">VDS_VOLUME_PROP2</a> structure instead of a <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a> structure.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>