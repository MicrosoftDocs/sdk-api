---
UID: NF:winddi.FONTOBJ_vGetInfo
title: FONTOBJ_vGetInfo function
author: windows-sdk-content
description: The FONTOBJ_vGetInfo function retrieves information about an associated font.
old-location: display\fontobj_vgetinfo.htm
old-project: display
ms.assetid: 4b952bdc-a496-4ded-9390-9f4b470f3a6c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: FONTOBJ_vGetInfo, FONTOBJ_vGetInfo function [Display Devices], display.fontobj_vgetinfo, gdifncs_0b07bb13-32b4-404c-824f-02f2b5659295.xml, winddi/FONTOBJ_vGetInfo
ms.prod: windows
ms.technology: windows-sdk
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
-	FONTOBJ_vGetInfo
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FONTOBJ_vGetInfo function


## -description


The <b>FONTOBJ_vGetInfo</b> function retrieves information about an associated font.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure to be queried.


### -param cjSize [in]

Specifies the size in bytes of the buffer pointed to by <i>pfi</i>.


### -param pfi

Pointer to a buffer previously allocated by the driver. GDI writes a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565970">FONTINFO</a> structure to this buffer.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565970">FONTINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

