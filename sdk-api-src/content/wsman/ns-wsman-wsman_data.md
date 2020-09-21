---
UID: NS:wsman._WSMAN_DATA
title: WSMAN_DATA (wsman.h)
description: Contains inbound and outbound data used in the Windows Remote Management (WinRM) API.
helpviewer_keywords: ["WSMAN_DATA","WSMAN_DATA structure [Windows Remote Management]","winrm.wsman_data","wsman/WSMAN_DATA"]
old-location: winrm\wsman_data.htm
tech.root: winrm
ms.assetid: 4ff574d4-04b0-47c3-808f-867d6815bffc
ms.date: 12/05/2018
ms.keywords: WSMAN_DATA, WSMAN_DATA structure [Windows Remote Management], winrm.wsman_data, wsman/WSMAN_DATA
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSMAN_DATA
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_DATA
 - wsman/_WSMAN_DATA
 - WSMAN_DATA
 - wsman/WSMAN_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_DATA
---

# WSMAN_DATA structure


## -description

Contains inbound and outbound data used in the Windows Remote Management (WinRM) API.

## -struct-fields

### -field type

Specifies the type of data currently stored in the union.

### -field text

### -field binaryData

### -field number

 




#### - ( unnamed union )

Contains the data.



#### text

If <b>type</b> is <b>WSMAN_DATA_TYPE_TEXT</b>,  <b>text</b> contains a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data_text">WSMAN_DATA_TEXT</a> structure.



#### binaryData

If <b>type</b> is <b>WSMAN_DATA_TYPE_XML_BINARY</b>, <b>binaryData</b> contains a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data_binary">WSMAN_DATA_BINARY</a> structure.



#### number

If <b>type</b> is <b>WSMAN_DATA_TYPE_DWORD</b>, <b>number</b> is a DWORD integer.