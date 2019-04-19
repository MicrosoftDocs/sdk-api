---
UID: NF:msvidctl.IMSVidCtl.get_DisplaySize
title: IMSVidCtl::get_DisplaySize (msvidctl.h)
author: windows-sdk-content
description: The get_DisplaySize method retrieves the display size.
old-location: mstv\imsvidctl_get_displaysize.htm
tech.root: mstv
ms.assetid: f3d5ed73-4781-46fb-8df4-a7dc339b755c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_DisplaySize method, IMSVidCtl.get_DisplaySize, IMSVidCtl::get_DisplaySize, IMSVidCtlget_DisplaySize, get_DisplaySize, get_DisplaySize method [Microsoft TV Technologies], get_DisplaySize method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_displaysize, msvidctl/IMSVidCtl::get_DisplaySize
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
 - IMSVidCtl.get_DisplaySize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidCtl::get_DisplaySize


## -description


The <b>get_DisplaySize</b> method retrieves the display size.


## -parameters




### -param CurrentValue [out]

Receives a member of the <a href="https://msdn.microsoft.com/2e939cbc-fc75-41d7-9fcb-32da5173f9bc">DisplaySizeList</a> enumeration.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The display size has no effect if the <b>AutoSize</b> property is false.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/8adbc701-fd05-4520-8f06-95bd67a08d1e">IMSVidCtl::get_AutoSize</a>



<a href="https://msdn.microsoft.com/1771e66b-e5f3-44f5-a489-e57baaf5cf25">IMSVidCtl::put_DisplaySize</a>
 

 

