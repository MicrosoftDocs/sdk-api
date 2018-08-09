---
UID: NE:mobsync._tagSYNCMGRITEMFLAGS
title: "_tagSYNCMGRITEMFLAGS"
author: windows-sdk-content
description: Specifies information for the current item in the SYNCMGRITEM structure.
old-location: shell\syncmgr_syncmgritemflags.htm
old-project: shell
ms.assetid: 6297f10b-9a2c-4077-9dca-e5c0850d125a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SYNCMGRITEMFLAGS, SYNCMGRITEMFLAGS enumeration [Windows Shell], SYNCMGRITEM_HASPROPERTIES, SYNCMGRITEM_HIDDEN, SYNCMGRITEM_LASTUPDATETIME, SYNCMGRITEM_MAYDELETEITEM, SYNCMGRITEM_ROAMINGUSER, SYNCMGRITEM_TEMPORARY, _tagSYNCMGRITEMFLAGS, mobsync/SYNCMGRITEMFLAGS, mobsync/SYNCMGRITEM_HASPROPERTIES, mobsync/SYNCMGRITEM_HIDDEN, mobsync/SYNCMGRITEM_LASTUPDATETIME, mobsync/SYNCMGRITEM_MAYDELETEITEM, mobsync/SYNCMGRITEM_ROAMINGUSER, mobsync/SYNCMGRITEM_TEMPORARY, shell.syncmgr_syncmgritemflags, syncmgr.syncmgritemflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SYNCMGRITEMFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mobsync.h
api_name:
 - SYNCMGRITEMFLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _tagSYNCMGRITEMFLAGS enumeration


## -description


Specifies information for the current item in the <a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a> structure.


## -enum-fields




### -field SYNCMGRITEM_HASPROPERTIES

The item has a properties dialog.


### -field SYNCMGRITEM_TEMPORARY

The item is temporary and any stored preferences can be removed. This value is defined but not used in Windows Vista.


### -field SYNCMGRITEM_ROAMINGUSER

The item roams with the user and is not specific to a machine. This value is defined but is ignored by both Windows XP and Windows Vista.
      


### -field SYNCMGRITEM_LASTUPDATETIME

The LastUpdateTime field is valid.


### -field SYNCMGRITEM_MAYDELETEITEM

The item may be deleted. This value has been deprecated for Windows Vista and later. This value is defined but is ignored by both Windows XP and Windows Vista.
      


### -field SYNCMGRITEM_HIDDEN

<b>Windows Vista and later</b>. Not supported.
      


## -see-also




<a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a>
 

 

