---
UID: NF:ocidl.IOleUndoUnit.GetUnitType
title: IOleUndoUnit::GetUnitType
author: windows-driver-content
description: Retrieves the CLSID and a type identifier for the undo unit.
old-location: com\ioleundounit_getunittype.htm
old-project: com
ms.assetid: 1f0c719e-75cd-48dd-8bd8-78eb63cc141a
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetUnitType, GetUnitType method [COM], GetUnitType method [COM],IOleUndoUnit interface, IOleUndoUnit interface [COM],GetUnitType method, IOleUndoUnit.GetUnitType, IOleUndoUnit::GetUnitType, _ole_ioleundounit_getunittype, com.ioleundounit_getunittype, ocidl/IOleUndoUnit::GetUnitType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IOleUndoUnit.GetUnitType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOleUndoUnit::GetUnitType


## -description


Retrieves the CLSID and a type identifier for the undo unit.


## -parameters




### -param pClsid [out]

A pointer to CLSID for the undo unit.


### -param plID [out]

A pointer to the type identifier for the undo unit.


## -returns



This method returns S_OK on success.




## -remarks



A parent undo unit can call this method on its child units to determine whether it can apply special handling to them. The CLSID returned can be the CLSID of the undo unit itself, of its creating object, or an arbitrary GUID. The undo unit has the option of returning CLSID_NULL, in which case the caller can make no assumptions about the type of this unit. The only requirement is that the CLSID and type identifier together uniquely identify this type of undo unit.

Note that the undo manager and parent undo units do not have the option of accepting or rejecting child units based on their type.




## -see-also




<a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a>
 

 

