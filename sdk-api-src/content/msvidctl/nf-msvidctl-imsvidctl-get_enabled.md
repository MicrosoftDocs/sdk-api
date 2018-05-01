---
UID: NF:msvidctl.IMSVidCtl.get_Enabled
title: IMSVidCtl::get_Enabled method
author: windows-driver-content
description: The get_Enabled method retrieves a value that determines whether the Video Control can respond to user-generated events.
old-location: mstv\imsvidctl_get_enabled.htm
old-project: mstv
ms.assetid: 7c1ec2a6-9880-4420-8d28-4374f1658bd9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidCtl, IMSVidCtl interface [Microsoft TV Technologies], get_Enabled method, IMSVidCtl::get_Enabled, IMSVidCtlget_Enabled, get_Enabled method [Microsoft TV Technologies], get_Enabled method [Microsoft TV Technologies], IMSVidCtl interface, get_Enabled,IMSVidCtl.get_Enabled, mstv.imsvidctl_get_enabled, msvidctl/IMSVidCtl::get_Enabled
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
-	IMSVidCtl.get_Enabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidCtl::get_Enabled method


## -description


The <b>get_Enabled</b> method retrieves a value that determines whether the Video Control can respond to user-generated events.


## -parameters




### -param pbool [out]

Variable of type <b>VARIANT_BOOL</b> that receives the current value of the property.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/366164ac-1514-46d6-870a-388706b8de75">IMSVidCtl::put_Enabled</a>
 

 

