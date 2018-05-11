---
UID: NF:msvidctl.IMSVidCtl.put_TabStop
title: IMSVidCtl::put_TabStop
author: windows-driver-content
description: The put_TabStop method specifies whether a user can use the TAB key to give the focus to the Video Control.
old-location: mstv\imsvidctl_put_tabstop.htm
old-project: mstv
ms.assetid: c0e3d216-ea3f-4db4-80fd-aaf4d520ba1a
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_TabStop method, IMSVidCtl.put_TabStop, IMSVidCtl::put_TabStop, IMSVidCtlput_TabStop, mstv.imsvidctl_put_tabstop, msvidctl/IMSVidCtl::put_TabStop, put_TabStop, put_TabStop method [Microsoft TV Technologies], put_TabStop method [Microsoft TV Technologies],IMSVidCtl interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msvidctl.h
req.include-header: 
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msvidctl.h
api_name:
-	IMSVidCtl.put_TabStop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidCtl::put_TabStop


## -description


The <b>put_TabStop</b> method specifies whether a user can use the TAB key to give the focus to the Video Control.


## -parameters




### -param vbool [in]

Specifies one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Include the Video Control in the tabbing order.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Do not include the Video Control in the tabbing order.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/9579144d-22b6-4d97-a52c-0d8bbc9066e4">IMSVidCtl::get_TabStop</a>
 

 

