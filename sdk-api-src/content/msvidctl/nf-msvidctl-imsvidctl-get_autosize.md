---
UID: NF:msvidctl.IMSVidCtl.get_AutoSize
title: IMSVidCtl::get_AutoSize
author: windows-sdk-content
description: The get_AutoSize method retrieves a value that determines whether the Video Control is automatically resized to display its entire contents.
old-location: mstv\imsvidctl_get_autosize.htm
tech.root: MSTV
ms.assetid: 8adbc701-fd05-4520-8f06-95bd67a08d1e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_AutoSize method, IMSVidCtl.get_AutoSize, IMSVidCtl::get_AutoSize, IMSVidCtlget_AutoSize, get_AutoSize, get_AutoSize method [Microsoft TV Technologies], get_AutoSize method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_autosize, msvidctl/IMSVidCtl::get_AutoSize
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
 - IMSVidCtl.get_AutoSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::get_AutoSize


## -description


The <b>get_AutoSize</b> method retrieves a value that determines whether the Video Control is automatically resized to display its entire contents.


## -parameters




### -param pbool [out]

Pointer to a variable of type <b>VARIANT_BOOL</b> that receives the current value of the property.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/eb5863e2-380b-4bee-ac18-e5f28551a6ab">IMSVidCtl::put_AutoSize</a>
 

 

