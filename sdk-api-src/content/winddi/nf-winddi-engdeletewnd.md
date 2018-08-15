---
UID: NF:winddi.EngDeleteWnd
title: EngDeleteWnd function
author: windows-sdk-content
description: The EngDeleteWnd function deletes a WNDOBJ structure.
old-location: display\engdeletewnd.htm
old-project: display
ms.assetid: bc6b3a61-18f6-4c7a-b6cb-a3f2dc4f6a36
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngDeleteWnd, EngDeleteWnd function [Display Devices], display.engdeletewnd, gdifncs_7a608897-cca5-45c9-94ea-afa7d3f6ed6a.xml, winddi/EngDeleteWnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
 - EngDeleteWnd
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngDeleteWnd function


## -description


The <b>EngDeleteWnd</b> function deletes a <a href="https://msdn.microsoft.com/69c47add-82a7-48fd-ae91-7756a6a8d15b">WNDOBJ</a> structure.


## -parameters




### -param pwo

Pointer to the WNDOBJ structure to be deleted.


## -returns



None




## -remarks



Because deleting a window object involves locking window resources, <b>EngDeleteWnd</b> should be called only in the context of the WNDOBJ_SETUP escape in <a href="https://msdn.microsoft.com/7b59dc85-27f4-4529-847e-6027dae8a45a">DrvEscape</a>, or from an <a href="https://msdn.microsoft.com/a1ec4764-4e11-4fb2-b439-ad6b721eb504">MCD</a> or <a href="https://msdn.microsoft.com/5a140cc0-ecc5-46ff-be3f-3c92f0f67dca">ICD</a> escape.

A driver can call <b>EngDeleteWnd</b> to remove its WNDOBJ structure associated with a window regardless of whether the window continues to exist. This is useful when the driver is being dynamically unloaded by the system while the associated window still exists.




## -see-also




<a href="https://msdn.microsoft.com/14b1cced-32d0-4ba8-be7c-e626bef37e3f">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/69c47add-82a7-48fd-ae91-7756a6a8d15b">WNDOBJ</a>
 

 

