---
UID: NF:iscsidsc.SetIScsiInitiatorNodeNameW
title: SetIScsiInitiatorNodeNameW function (iscsidsc.h)
description: SetIscsiInitiatorNodeName function establishes an initiator node name for the computer. This name is utilized by any initiator nodes on the computer that are communicating with other nodes.helpviewer_keywords: ["SetIScsiInitiatorNodeNameW","SetIscsiInitiatorNodeName","SetIscsiInitiatorNodeName function [iSCSI Discovery Library API]","SetIscsiInitiatorNodeNameA","SetIscsiInitiatorNodeNameW","iscsidisc.setiscsiinitiatornodename","iscsidsc/SetIscsiInitiatorNodeName","iscsidsc/SetIscsiInitiatorNodeNameA","iscsidsc/SetIscsiInitiatorNodeNameW"]
old-location: iscsidisc\setiscsiinitiatornodename.htm
tech.root: iSCSIDisc
ms.assetid: 4758fbde-da94-4da2-9c04-d2bec2c61752
ms.date: 12/05/2018
ms.keywords: SetIScsiInitiatorNodeNameW, SetIscsiInitiatorNodeName, SetIscsiInitiatorNodeName function [iSCSI Discovery Library API], SetIscsiInitiatorNodeNameA, SetIscsiInitiatorNodeNameW, iscsidisc.setiscsiinitiatornodename, iscsidsc/SetIscsiInitiatorNodeName, iscsidsc/SetIscsiInitiatorNodeNameA, iscsidsc/SetIscsiInitiatorNodeNameW
f1_keywords:
- iscsidsc/SetIscsiInitiatorNodeName
dev_langs:
- c++
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetIscsiInitiatorNodeNameW (Unicode) and SetIscsiInitiatorNodeNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Iscsidsc.dll
api_name:
- SetIscsiInitiatorNodeName
- SetIscsiInitiatorNodeNameA
- SetIscsiInitiatorNodeNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetIScsiInitiatorNodeNameW function


## -description


The <b>SetIscsiInitiatorNodeName</b> function establishes an initiator node name for the computer. This name is utilized by  any initiator nodes on the computer that are communicating with other nodes.



## -parameters




### -param InitiatorNodeName

The initiator node name. If this parameter is <b>null</b>, initiators use a default initiator node name based upon the computer name.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



The <b>SetIscsiInitiatorNodeName</b> routine does not verify that the format of the name in <i>InitiatorNodeName</i> is correct.

Some hardware initiator drivers can respond immediately to a change of the node name, while others must be restarted to finalize the change to the node name.





