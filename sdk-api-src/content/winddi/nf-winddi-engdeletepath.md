---
UID: NF:winddi.EngDeletePath
title: EngDeletePath function
author: windows-sdk-content
description: The EngDeletePath function deletes a path previously allocated by EngCreatePath.
old-location: display\engdeletepath.htm
old-project: display
ms.assetid: 65ecf4bc-5180-4b4b-a359-298f385b849e
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: EngDeletePath, EngDeletePath function [Display Devices], display.engdeletepath, gdifncs_aa1e2ccc-cc76-4782-b2ff-9867576c82d1.xml, winddi/EngDeletePath
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngDeletePath
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngDeletePath function


## -description


The <b>EngDeletePath</b> function deletes a path previously allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564755">EngCreatePath</a>.


## -parameters




### -param ppo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure to be deleted.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564755">EngCreatePath</a>
 

 

