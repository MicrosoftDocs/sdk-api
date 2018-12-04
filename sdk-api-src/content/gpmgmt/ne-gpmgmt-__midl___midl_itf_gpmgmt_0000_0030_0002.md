---
UID: NE:gpmgmt.__MIDL___MIDL_itf_gpmgmt_0000_0030_0002
title: "__MIDL___MIDL_itf_gpmgmt_0000_0030_0002"
author: windows-sdk-content
description: The Starter Group Policy object is a system Starter Group Policy object or a custom Starter Group Policy object.
old-location: gpmc\gpmstartergpotype.htm
tech.root: gpmc
ms.assetid: 19b84c06-d8dc-4a25-85f6-cfbe9937f30e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GPMStarterGPOType, GPMStarterGPOType enumeration [GPMC], __MIDL___MIDL_itf_gpmgmt_0000_0030_0002, gpmc.gpmstartergpotype, gpmgmt/GPMStarterGPOType, gpmgmt/typeCustom, gpmgmt/typeSystem, typeCustom, typeSystem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
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
 - HeaderDef
api_location:
 - gpmgmt.h
api_name:
 - GPMStarterGPOType
product: Windows
targetos: Windows
req.typenames: GPMStarterGPOType
req.redist: 
---

# __MIDL___MIDL_itf_gpmgmt_0000_0030_0002 enumeration


## -description


<b>GPMStarterGPOType</b> defines if  the Starter Group Policy object is a system  Starter Group Policy object or a custom Starter Group Policy object.

<b>GPMStarterGPOType</b> defines if   the Starter Group Policy object is a system  Starter Group Policy object or a custom Starter Group Policy object.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef enum {
        typeSystem = 0,
        typeCustom
} GPMStarterGPOType;</pre>
</td>
</tr>
</table></span></div>

## -enum-fields




### -field typeSystem

A system Starter Group Policy object


### -field typeCustom

A  custom Starter Group Policy object

