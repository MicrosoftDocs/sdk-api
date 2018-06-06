---
UID: NF:winddi.EngFindResource
title: EngFindResource function
author: windows-sdk-content
description: The EngFindResource function determines the location of a resource in a module.
old-location: display\engfindresource.htm
old-project: display
ms.assetid: f83d9112-af06-4b73-84b3-5b1c5b3daffb
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngFindResource, EngFindResource function [Display Devices], display.engfindresource, gdifncs_93a3a136-5dfb-4c3c-afbc-4a1c475ae0c6.xml, winddi/EngFindResource
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngFindResource
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngFindResource function


## -description


The <b>EngFindResource</b> function determines the location of a resource in a module.


## -parameters




### -param h [in]

Handle to the module that contains the resource. This handle is obtained from <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>.


### -param iName [in]

Is an integer identifier representing the name of the resource being looked up.


### -param iType [in]

Is an integer identifier representing the type of the resource being looked up.


### -param pulSize [out]

Pointer to a ULONG in which the resource's size, in bytes, is returned.


## -returns



The return value is a pointer to the address of the specified resource. The function returns <b>NULL</b> if an error occurs.




## -remarks



The size of a successfully located resource is returned in <i>pulSize</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564974">EngMapModule</a>
 

 

