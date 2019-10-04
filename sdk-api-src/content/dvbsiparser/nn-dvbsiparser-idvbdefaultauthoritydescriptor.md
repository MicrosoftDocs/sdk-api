---
UID: NN:dvbsiparser.IDvbDefaultAuthorityDescriptor
title: IDvbDefaultAuthorityDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from the default authority descriptor for a content reference identifier (CRID). The default authority descriptor is the first part of the CRID and identifies the body that created the CRID.
old-location: mstv\idvbdefaultauthoritydescriptor.htm
tech.root: mstv
ms.assetid: 42d10cb5-dea9-4fdb-a588-7bc647e0b95b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvbDefaultAuthorityDescriptor, IDvbDefaultAuthorityDescriptor interface [Microsoft TV Technologies], IDvbDefaultAuthorityDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbDefaultAuthorityDescriptor, mstv.idvbdefaultauthoritydescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IDvbDefaultAuthorityDescriptor"
dev_langs:
 - c++
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - dvbsiparser.h
api_name:
 - IDvbDefaultAuthorityDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbDefaultAuthorityDescriptor interface


## -description


Implements methods that get data from the default authority descriptor for a content reference identifier (CRID). 
The default authority descriptor is the first part of the CRID and identifies the body that created the CRID.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbDefaultAuthorityDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbDefaultAuthorityDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbDefaultAuthorityDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdefaultauthoritydescriptor-getdefaultauthority">GetDefaultAuthority</a>
</td>
<td align="left" width="63%">
Gets the string identifying the default authority from a  DVB  CRID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdefaultauthoritydescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB  default authority descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbdefaultauthoritydescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB  default authority descriptor.

</td>
</tr>
</table> 

