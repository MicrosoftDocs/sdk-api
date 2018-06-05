---
UID: NE:objbase.tagCOMSD
title: tagCOMSD
author: windows-sdk-content
description: Determines the type of COM security descriptor to get when calling CoGetSystemSecurityPermissions.
old-location: com\comsd.htm
old-project: com
ms.assetid: FF783F27-D5EF-4927-9B7D-489271FBA9B3
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: COMSD, COMSD enumeration [COM], SD_ACCESSPERMISSIONS, SD_ACCESSRESTRICTIONS, SD_LAUNCHPERMISSIONS, SD_LAUNCHRESTRICTIONS, com.comsd, objbase/COMSD, objbase/SD_ACCESSPERMISSIONS, objbase/SD_ACCESSRESTRICTIONS, objbase/SD_LAUNCHPERMISSIONS, objbase/SD_LAUNCHRESTRICTIONS, tagCOMSD
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: COMSD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Objbase.h
api_name:
-	COMSD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagCOMSD enumeration


## -description


Determines the type of COM security descriptor to get when calling <a href="https://msdn.microsoft.com/8210A6A0-B861-4E85-8E5A-1BF82A01C54E">CoGetSystemSecurityPermissions</a>.


## -enum-fields




### -field SD_LAUNCHPERMISSIONS

Machine-wide launch permissions.


### -field SD_ACCESSPERMISSIONS

Machine-wide access permissions.


### -field SD_LAUNCHRESTRICTIONS

Machine-wide launch limits.


### -field SD_ACCESSRESTRICTIONS

Machine-wide access limits.


## -see-also




<a href="https://msdn.microsoft.com/8210A6A0-B861-4E85-8E5A-1BF82A01C54E">CoGetSystemSecurityPermissions</a>
 

 

