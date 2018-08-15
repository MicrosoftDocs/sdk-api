---
UID: NF:msvidctl.IMSVidCtl.get_TabStop
title: IMSVidCtl::get_TabStop
author: windows-sdk-content
description: The get_TabStop method queries whether a user can use the TAB key to give the focus to the Video Control.
old-location: mstv\imsvidctl_get_tabstop.htm
old-project: mstv
ms.assetid: 9579144d-22b6-4d97-a52c-0d8bbc9066e4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_TabStop method, IMSVidCtl.get_TabStop, IMSVidCtl::get_TabStop, IMSVidCtlget_TabStop, get_TabStop, get_TabStop method [Microsoft TV Technologies], get_TabStop method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_tabstop, msvidctl/IMSVidCtl::get_TabStop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_TabStop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::get_TabStop


## -description


The <b>get_TabStop</b> method queries whether a user can use the TAB key to give the focus to the Video Control.


## -parameters




### -param pbool [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The Video Control is in the tabbing order.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The Video Control is not in the tabbing order.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/c0e3d216-ea3f-4db4-80fd-aaf4d520ba1a">IMSVidCtl::put_TabStop</a>
 

 

