---
UID: NF:winddi.STROBJ_vEnumStart
title: STROBJ_vEnumStart function
author: windows-driver-content
description: The STROBJ_vEnumStart function defines the form, or type, for data that will be returned from GDI in subsequent calls to STROBJ_bEnum.
old-location: display\strobj_venumstart.htm
old-project: display
ms.assetid: 568af273-2b9d-4782-849f-6cb9c49952e0
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: STROBJ_vEnumStart, STROBJ_vEnumStart function [Display Devices], display.strobj_venumstart, gdifncs_f0be3fdf-8725-4f9c-8487-0aaa95a13ede.xml, winddi/STROBJ_vEnumStart
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	STROBJ_vEnumStart
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# STROBJ_vEnumStart function


## -description


The <b>STROBJ_vEnumStart</b> function defines the form, or type, for data that will be returned from GDI in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff569739">STROBJ_bEnum</a>. 


## -parameters




### -param pstro

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a> structure whose data form is to be defined.


## -returns



None




## -remarks



This function also restarts the enumeration of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a> array.

This function should be called by the driver prior to calling <b>STROBJ_bEnum</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569739">STROBJ_bEnum</a>
 

 

