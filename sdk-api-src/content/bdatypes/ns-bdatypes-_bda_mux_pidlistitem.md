---
UID: NS:bdatypes._BDA_MUX_PIDLISTITEM
title: "_BDA_MUX_PIDLISTITEM"
author: windows-driver-content
description: Specifies a packet identifier (PID) for the IBDA_MUX interface.
old-location: mstv\bda_mux_pidlistitem.htm
old-project: mstv
ms.assetid: 50355317-7133-445c-9990-ab536801e555
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PBDA_MUX_PIDLISTITEM, BDA_MUX_PIDLISTITEM, BDA_MUX_PIDLISTITEM structure [Microsoft TV Technologies], PBDA_MUX_PIDLISTITEM, PBDA_MUX_PIDLISTITEM structure pointer [Microsoft TV Technologies], _BDA_MUX_PIDLISTITEM, bdatypes/BDA_MUX_PIDLISTITEM, bdatypes/PBDA_MUX_PIDLISTITEM, mstv.bda_mux_pidlistitem"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdatypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BDA_MUX_PIDLISTITEM, *PBDA_MUX_PIDLISTITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdatypes.h
api_name:
-	BDA_MUX_PIDLISTITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BDA_MUX_PIDLISTITEM structure


## -description


Specifies a packet identifier (PID) for the <a href="https://msdn.microsoft.com/5dde7b14-d5a4-4db5-b91f-d6bfd4be269d">IBDA_MUX</a> interface.


## -struct-fields




### -field usPIDNumber

The PID number.


### -field usProgramNumber

The associated service identifier, if applicable.


### -field ePIDType

The stream type, specified as a member of the <a href="https://msdn.microsoft.com/2db22de7-9b82-4894-a6f3-5a73ab5efb7d">MUX_PID_TYPE</a> enumeration.


## -see-also




<a href="https://msdn.microsoft.com/5dde7b14-d5a4-4db5-b91f-d6bfd4be269d">IBDA_MUX</a>
 

 

