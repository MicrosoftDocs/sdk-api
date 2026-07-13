---
UID: NF:objidlbase.IPipeLong.Pull
title: IPipeLong::Pull (objidlbase.h)
description: The IPipeLong::Pull (objidlbase.h) method retrieves data of the long integer type from the pipe source.
helpviewer_keywords: ["IPipeLong interface [COM]","Pull method","IPipeLong.Pull","IPipeLong::Pull","Pull","Pull method [COM]","Pull method [COM]","IPipeLong interface","_com_ipipelong_pull","com.ipipelong_pull","objidlbase/IPipeLong::Pull"]
old-location: com\ipipelong_pull.htm
tech.root: com
ms.assetid: 33da8bd7-3350-4f6e-84f8-3046da226d2f
ms.date: 08/13/2022
ms.keywords: IPipeLong interface [COM],Pull method, IPipeLong.Pull, IPipeLong::Pull, Pull, Pull method [COM], Pull method [COM],IPipeLong interface, _com_ipipelong_pull, com.ipipelong_pull, objidlbase/IPipeLong::Pull
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPipeLong::Pull
 - objidlbase/IPipeLong::Pull
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IPipeLong.Pull
---

# IPipeLong::Pull


## -description

Retrieves data of the long integer type from the pipe source.

## -parameters

### -param buf [out]

A pointer to the memory buffer that receives the data. The buffer must be able to hold at least the number of long integers specified in <i>cRequest</i>.

### -param cRequest [in]

The number of long integers requested.

### -param pcReturned [out]

The actual number of long integers returned.

## -returns

This method returns S_OK to indicate that the data was retrieved successfully.

## -remarks

When the <b>Pull</b> method is called, data is requested from the provider of the pipe. The caller must provide a buffer that will hold at least the number of long integers specified in the <i>cRequest</i> parameter. The proxy will unmarshal the data into the provided buffer and set the number of long integers actually provided in <i>pcReturned</i>. The <i>pcReturned</i> parameter can be less than or equal to <i>cRequest</i>, but it will never be greater. When <i>pcReturned</i> is 0, it indicates that there is no more data.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipipelong">IPipeLong</a>
