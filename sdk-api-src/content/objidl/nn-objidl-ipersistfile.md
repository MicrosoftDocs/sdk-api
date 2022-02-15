---
UID: NN:objidl.IPersistFile
title: IPersistFile (objidl.h)
description: Enables an object to be loaded from or saved to a disk file, rather than a storage object or stream.
helpviewer_keywords: ["IPersistFile","IPersistFile interface [COM]","IPersistFile interface [COM]","described","_com_ipersistfile","com.ipersistfile","objidl/IPersistFile"]
old-location: com\ipersistfile.htm
tech.root: com
ms.assetid: 7d34507f-8a16-43b4-8225-010798abc546
ms.date: 12/05/2018
ms.keywords: IPersistFile, IPersistFile interface [COM], IPersistFile interface [COM],described, _com_ipersistfile, com.ipersistfile, objidl/IPersistFile
req.header: objidl.h
req.include-header: 
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
 - IPersistFile
 - objidl/IPersistFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistFile
---

# IPersistFile interface


## -description

Enables an object to be loaded from or saved to a disk file, rather than a storage object or stream. Because the information needed to open a file varies greatly from one application to another, the implementation of <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">IPersistFile::Load</a> on the object must also open its disk file.

## -inheritance

The <b>IPersistFile</b> interface inherits from <b>IPersist</b>. <b>IPersistFile</b> also has these types of members:

