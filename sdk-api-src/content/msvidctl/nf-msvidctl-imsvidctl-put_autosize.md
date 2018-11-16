---
UID: NF:msvidctl.IMSVidCtl.put_AutoSize
title: IMSVidCtl::put_AutoSize
author: windows-sdk-content
description: The put_AutoSize method specifies whether the Video Control automatically resizes to display its entire contents.
old-location: mstv\imsvidctl_put_autosize.htm
tech.root: mstv
ms.assetid: eb5863e2-380b-4bee-ac18-e5f28551a6ab
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_AutoSize method, IMSVidCtl.put_AutoSize, IMSVidCtl::put_AutoSize, IMSVidCtlput_AutoSize, mstv.imsvidctl_put_autosize, msvidctl/IMSVidCtl::put_AutoSize, put_AutoSize, put_AutoSize method [Microsoft TV Technologies], put_AutoSize method [Microsoft TV Technologies],IMSVidCtl interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.put_AutoSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msvidctl.h
: 
- IMSVidCtl.put_AutoSize
: 
---

# IMSVidCtl::put_AutoSize


## -description


The <b>put_AutoSize</b> method specifies whether the Video Control automatically resizes to display its entire contents.


## -parameters




### -param vbool [in]

Specifies whether the Video Control automatically resizes. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The Video Control automatically resizes.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The Video Control does not automatically resize.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/8adbc701-fd05-4520-8f06-95bd67a08d1e">IMSVidCtl::get_AutoSize</a>
 

 

