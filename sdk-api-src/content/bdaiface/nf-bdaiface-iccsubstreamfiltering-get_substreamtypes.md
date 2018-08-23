---
UID: NF:bdaiface.ICCSubStreamFiltering.get_SubstreamTypes
title: ICCSubStreamFiltering::get_SubstreamTypes
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iccsubstreamfiltering_get_substreamtypes.htm
old-project: mstv
ms.assetid: da622981-d2a6-4e91-9e59-b084932b5ff2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ICCSubStreamFiltering interface [Microsoft TV Technologies],get_SubstreamTypes method, ICCSubStreamFiltering.get_SubstreamTypes, ICCSubStreamFiltering::get_SubstreamTypes, ICCSubStreamFilteringget_SubstreamTypes, bdaiface/ICCSubStreamFiltering::get_SubstreamTypes, get_SubstreamTypes, get_SubstreamTypes method [Microsoft TV Technologies], get_SubstreamTypes method [Microsoft TV Technologies],ICCSubStreamFiltering interface, mstv.iccsubstreamfiltering_get_substreamtypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - ICCSubStreamFiltering.get_SubstreamTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICCSubStreamFiltering::get_SubstreamTypes


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>get_SubstreamTypes</b> method retrieves the list of closed captioning services this pin is delivering.


## -parameters




### -param pTypes [out]

Receives a bitwise OR of flags that specify the closed captioning services. For a list of flags, see <a href="https://msdn.microsoft.com/en-us/library/Dd695076(v=VS.85).aspx">KS_CC_SUBSTREAM Constants</a>.


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
 

 

