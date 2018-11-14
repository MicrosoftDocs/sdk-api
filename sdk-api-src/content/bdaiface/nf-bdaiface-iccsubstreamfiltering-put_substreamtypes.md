---
UID: NF:bdaiface.ICCSubStreamFiltering.put_SubstreamTypes
title: ICCSubStreamFiltering::put_SubstreamTypes
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iccsubstreamfiltering_put_substreamtypes.htm
tech.root: MSTV
ms.assetid: 45db472d-cffc-42d1-8270-3a0db72bdc2c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICCSubStreamFiltering interface [Microsoft TV Technologies],put_SubstreamTypes method, ICCSubStreamFiltering.put_SubstreamTypes, ICCSubStreamFiltering::put_SubstreamTypes, ICCSubStreamFilteringput_SubstreamTypes, bdaiface/ICCSubStreamFiltering::put_SubstreamTypes, mstv.iccsubstreamfiltering_put_substreamtypes, put_SubstreamTypes, put_SubstreamTypes method [Microsoft TV Technologies], put_SubstreamTypes method [Microsoft TV Technologies],ICCSubStreamFiltering interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
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
 - bdaiface.h
api_name:
 - ICCSubStreamFiltering.put_SubstreamTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdaiface.h
: 
- ICCSubStreamFiltering.put_SubstreamTypes
: 
---

# ICCSubStreamFiltering::put_SubstreamTypes


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>get_SubstreamTypes</b> method sets the closed captioning services the pin will deliver.


## -parameters




### -param Types [in]

Bitwise OR of flags that specify the closed captioning services. For a list of flags, see <a href="https://msdn.microsoft.com/en-us/library/Dd695076(v=VS.85).aspx">KS_CC_SUBSTREAM Constants</a>. Any services that are not selected are simply dropped.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693501(v=VS.85).aspx">ICCSubStreamFiltering Interface</a>
 

 

