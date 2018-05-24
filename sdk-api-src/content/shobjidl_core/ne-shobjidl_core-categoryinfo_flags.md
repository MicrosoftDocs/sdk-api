---
UID: NE:shobjidl_core.CATEGORYINFO_FLAGS
title: CATEGORYINFO_FLAGS
author: windows-driver-content
description: Provides a set of flags for use with the CATEGORY_INFO structure.
old-location: shell\CATEGORYINFO_FLAGS.htm
old-project: shell
ms.assetid: 6179ed67-905a-454a-a226-fe1e5070e39f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: CATEGORYINFO_FLAGS, CATEGORYINFO_FLAGS enumeration [Windows Shell], CATINFO_COLLAPSED, CATINFO_EXPANDED, CATINFO_HIDDEN, CATINFO_NOHEADER, CATINFO_NOHEADERCOUNT, CATINFO_NORMAL, CATINFO_NOTCOLLAPSIBLE, CATINFO_SUBSETTED, inet_CATEGORYINFO_FLAGS, shell.CATEGORYINFO_FLAGS, shobjidl_core/CATEGORYINFO_FLAGS, shobjidl_core/CATINFO_COLLAPSED, shobjidl_core/CATINFO_EXPANDED, shobjidl_core/CATINFO_HIDDEN, shobjidl_core/CATINFO_NOHEADER, shobjidl_core/CATINFO_NOHEADERCOUNT, shobjidl_core/CATINFO_NORMAL, shobjidl_core/CATINFO_NOTCOLLAPSIBLE, shobjidl_core/CATINFO_SUBSETTED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CATEGORYINFO_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shobjidl_core.h
api_name:
-	CATEGORYINFO_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# CATEGORYINFO_FLAGS enumeration


## -description


Provides a set of flags for use with the <a href="https://msdn.microsoft.com/6198cd31-94db-4d31-9cc9-f8b90e661809">CATEGORY_INFO</a> structure.


## -enum-fields




### -field CATINFO_NORMAL

0x00000000. Applies default properties for the category.


### -field CATINFO_COLLAPSED

0x00000001. The category should appear as collapsed


### -field CATINFO_HIDDEN

0x00000002. The category should appear as hidden.


### -field CATINFO_EXPANDED

0x00000004. The category should appear as expanded.


### -field CATINFO_NOHEADER

0x00000008. The category has no header.


### -field CATINFO_NOTCOLLAPSIBLE

0x00000010. The category cannot be collapsed.


### -field CATINFO_NOHEADERCOUNT

0x00000020. The count of items in the category should not be displayed in the header.


### -field CATINFO_SUBSETTED

0x00000040. <b>Windows 7 and later</b>. The category should appear subsetted.


### -field CATINFO_SEPARATE_IMAGES


### -field CATINFO_SHOWEMPTY



