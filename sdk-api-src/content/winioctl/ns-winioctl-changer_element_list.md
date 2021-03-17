---
UID: NS:winioctl._CHANGER_ELEMENT_LIST
title: CHANGER_ELEMENT_LIST
description: Represents a range of elements of a single type, typically for an operation such as getting or initializing the status of multiple elements.
helpviewer_keywords: ["*PCHANGER_ELEMENT_LIST","CHANGER_ELEMENT_LIST","CHANGER_ELEMENT_LIST structure","PCHANGER_ELEMENT_LIST","PCHANGER_ELEMENT_LIST structure pointer","_win32_changer_element_list_str","base.changer_element_list_str","winioctl/CHANGER_ELEMENT_LIST","winioctl/PCHANGER_ELEMENT_LIST"]
old-location: base\changer_element_list_str.htm
tech.root: base
ms.assetid: cb1fcf78-b36a-4551-8eeb-da58edc80890
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_ELEMENT_LIST, CHANGER_ELEMENT_LIST, CHANGER_ELEMENT_LIST structure, PCHANGER_ELEMENT_LIST, PCHANGER_ELEMENT_LIST structure pointer, _win32_changer_element_list_str, base.changer_element_list_str, winioctl/CHANGER_ELEMENT_LIST, winioctl/PCHANGER_ELEMENT_LIST'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: CHANGER_ELEMENT_LIST, *PCHANGER_ELEMENT_LIST
req.redist: 
f1_keywords:
 - _CHANGER_ELEMENT_LIST
 - winioctl/_CHANGER_ELEMENT_LIST
 - PCHANGER_ELEMENT_LIST
 - winioctl/PCHANGER_ELEMENT_LIST
 - CHANGER_ELEMENT_LIST
 - winioctl/CHANGER_ELEMENT_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CHANGER_ELEMENT_LIST
---

# CHANGER_ELEMENT_LIST structure


## -description

Represents a range of elements of a single type, typically for an operation such as getting or initializing the status of multiple elements.

## -struct-fields

### -field Element

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that represent the first element in the range.

### -field NumberOfElements

The number of elements in the range.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_reinitialize_transport">IOCTL_CHANGER_REINITIALIZE_TRANSPORT</a>