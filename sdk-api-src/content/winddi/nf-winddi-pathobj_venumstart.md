---
UID: NF:winddi.PATHOBJ_vEnumStart
title: PATHOBJ_vEnumStart function
author: windows-sdk-content
description: The PATHOBJ_vEnumStart function notifies a given PATHOBJ structure that the driver will be calling PATHOBJ_bEnum to enumerate lines and/or curves in the path.
old-location: display\pathobj_venumstart.htm
old-project: display
ms.assetid: b83e6f87-be79-4743-bc52-b9310853c4f5
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PATHOBJ_vEnumStart, PATHOBJ_vEnumStart function [Display Devices], display.pathobj_venumstart, gdifncs_93ed4330-ebfd-4ba1-b095-99beb3146452.xml, winddi/PATHOBJ_vEnumStart
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
-	PATHOBJ_vEnumStart
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# PATHOBJ_vEnumStart function


## -description


The <b>PATHOBJ_vEnumStart</b> function notifies a given PATHOBJ structure that the driver will be calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff568851">PATHOBJ_bEnum</a> to enumerate lines and/or curves in the path.


## -parameters




### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure whose lines and/or curves are to be enumerated.


## -returns



None




## -remarks



<b>PATHOBJ_vEnumStart</b> can be called at any time to restart an enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568851">PATHOBJ_bEnum</a>
 

 

