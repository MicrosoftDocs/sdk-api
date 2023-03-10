---
UID: NF:objidlbase.IPipeLong.Push
title: IPipeLong::Push (objidlbase.h)
description: The IPipeLong::Push (objidlbase.h) method sends data of the long integer type to the pipe source.
helpviewer_keywords: ["IPipeLong interface [COM]","Push method","IPipeLong.Push","IPipeLong::Push","Push","Push method [COM]","Push method [COM]","IPipeLong interface","_com_ipipelong_push","com.ipipelong_push","objidlbase/IPipeLong::Push"]
old-location: com\ipipelong_push.htm
tech.root: com
ms.assetid: 16389e32-74f9-419b-bcc5-63fe43b3e456
ms.date: 08/13/2022
ms.keywords: IPipeLong interface [COM],Push method, IPipeLong.Push, IPipeLong::Push, Push, Push method [COM], Push method [COM],IPipeLong interface, _com_ipipelong_push, com.ipipelong_push, objidlbase/IPipeLong::Push
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
 - IPipeLong::Push
 - objidlbase/IPipeLong::Push
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
 - IPipeLong.Push
---

# IPipeLong::Push


## -description

Sends data of the long integer type to the pipe source.

## -parameters

### -param buf [in]

A pointer to the memory buffer that holds the data to be sent.

### -param cSent [in]

The number of long integers in the buffer.

## -returns

This method returns S_OK to indicate that the data was sent successfully.

## -remarks

When the <b>Push</b> method is called, the data is being sent to the provider of the pipe. The caller fills the buffer with the data and then calls <b>Push</b>. The number of long integers being sent is specified in the <i>cSent</i> parameter. The caller is responsible for ensuring that the buffer is valid for the duration of the call.

When the last of the data has been pushed, the caller must do one last push of <i>cSent</i> equal to 0 to indicate that the data transfer is complete.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipipelong">IPipeLong</a>
