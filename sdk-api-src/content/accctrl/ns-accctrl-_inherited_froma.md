---
UID: NS:accctrl._INHERITED_FROMA
title: "_INHERITED_FROMA"
author: windows-sdk-content
description: Provides information about an object's inherited access control entry (ACE).
old-location: security\inherited_from.htm
old-project: SecAuthZ
ms.assetid: 6839f67a-6c72-406d-b55e-bc366aaad107
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PINHERITED_FROMA, INHERITED_FROM, INHERITED_FROM structure [Security], INHERITED_FROMA, INHERITED_FROMW, PINHERITED_FROM, PINHERITED_FROM structure pointer [Security], _INHERITED_FROMA, _INHERITED_FROMW, accctrl/INHERITED_FROM, accctrl/INHERITED_FROMA, accctrl/INHERITED_FROMW, accctrl/PINHERITED_FROM, security.inherited_from"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: INHERITED_FROMW (Unicode) and INHERITED_FROMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: INHERITED_FROMA, *PINHERITED_FROMA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	AccCtrl.h
api_name:
-	INHERITED_FROM
-	INHERITED_FROMA
-	INHERITED_FROMW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
---

# _INHERITED_FROMA structure


## -description


The <b>INHERITED_FROM</b> structure provides information about an object's inherited <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE).


## -struct-fields




### -field GenerationGap

Number of levels, or generations, between the object and the ancestor. Set this to zero for an explicit ACE. If the ancestor cannot be determined for the inherited ACE, set this member to –1.


### -field AncestorName

Name of the ancestor from which the ACE was inherited. For an explicit ACE, set this to <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/c9c58b9a-1b65-40e2-b518-30e247f9718e">FreeInheritedFromArray</a>



<a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a>
 

 

