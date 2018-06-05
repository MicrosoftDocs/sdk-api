---
UID: NF:winddi.EngDeleteSurface
title: EngDeleteSurface function
author: windows-sdk-content
description: The EngDeleteSurface function deletes the specified surface.
old-location: display\engdeletesurface.htm
old-project: display
ms.assetid: 9cde6fa3-26b6-49fd-9374-cbf91215aa39
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngDeleteSurface, EngDeleteSurface function [Display Devices], display.engdeletesurface, gdifncs_7ffbac74-6789-4f81-a4eb-4f6f1c41a444.xml, winddi/EngDeleteSurface
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngDeleteSurface
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngDeleteSurface function


## -description


The <b>EngDeleteSurface</b> function deletes the specified surface.


## -parameters




### -param hsurf [in]

Handle to the surface to delete. This handle can be an HSURF or HBM.


## -returns



<b>EngDeleteSurface</b> returns <b>TRUE</b> if it is successful in deleting the surface. Otherwise, it returns <b>FALSE</b> and an error code is logged.



