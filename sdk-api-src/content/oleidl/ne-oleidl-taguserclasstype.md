---
UID: NE:oleidl.tagUSERCLASSTYPE
title: tagUSERCLASSTYPE
author: windows-sdk-content
description: Indicates the different variants of the display name associated with a class of objects.
old-location: com\userclasstype.htm
old-project: com
ms.assetid: f35dd18a-7fde-4954-8315-bc9bfd933827
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: USERCLASSTYPE, USERCLASSTYPE enumeration [COM], USERCLASSTYPE_APPNAME, USERCLASSTYPE_FULL, USERCLASSTYPE_SHORT, _ole_USERCLASSTYPE, com.userclasstype, oleidl/USERCLASSTYPE, oleidl/USERCLASSTYPE_APPNAME, oleidl/USERCLASSTYPE_FULL, oleidl/USERCLASSTYPE_SHORT, tagUSERCLASSTYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIVIEWPROPSW (Unicode) and OLEUIVIEWPROPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - USERCLASSTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagUSERCLASSTYPE enumeration


## -description


Indicates the different variants of the display name associated with a class of objects.


## -enum-fields




### -field USERCLASSTYPE_FULL

The full type name of the class.


### -field USERCLASSTYPE_SHORT

A short name (maximum of 15 characters) that is used for popup menus and the <b>Links</b> dialog box.


### -field USERCLASSTYPE_APPNAME

The name of the application servicing the class and is used in the result text in dialog boxes.


## -see-also




<a href="https://msdn.microsoft.com/8ffffa01-d118-4955-84d1-a4659ba9ddc9">IOleObject::GetUserType</a>



<a href="https://msdn.microsoft.com/492a4084-494e-4d78-8f3a-853ec486a2d6">OleRegGetUserType</a>
 

 

