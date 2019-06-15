---
UID: NS:wabdefs._ADRLIST
title: ADRLIST (wabdefs.h)
author: windows-sdk-content
description: Do not use. Describes zero or more properties belonging to one or more recipients.
old-location: wab\_wab_ADRLIST.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\adrlist.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPADRLIST, ADRLIST, ADRLIST structure [Windows Address Book], Gender, Gender structure [Windows Address Book], _wab_ADRLIST, wab._wab_ADRLIST, wabdefs/ADRLIST"
ms.topic: struct
req.header: wabdefs.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - Gender
product: Windows
targetos: Windows
req.typenames: ADRLIST, *LPADRLIST
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# ADRLIST structure


## -description


Do not use. Describes zero or more properties belonging to one or more recipients. 



## -struct-fields




### -field cEntries

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the entry count in the array specified by the <b>aEntries</b> member.


### -field aEntries

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wabdefs/ns-wabdefs-_adrentry">ADRENTRY</a>[MAPI_DIM]</b>

Variable of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wabdefs/ns-wabdefs-_adrentry">ADRENTRY</a> that specifies the array of <b>ADRENTRY</b> structures, one structure for each recipient.

