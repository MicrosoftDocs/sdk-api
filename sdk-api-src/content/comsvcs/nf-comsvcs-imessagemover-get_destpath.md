---
UID: NF:comsvcs.IMessageMover.get_DestPath
title: IMessageMover::get_DestPath (comsvcs.h)
description: Retrieves the path of the destination (output) queue.
helpviewer_keywords: ["IMessageMover interface [COM+]","get_DestPath method","IMessageMover.get_DestPath","IMessageMover::get_DestPath","comsvcs/IMessageMover::get_DestPath","cos.imessagemover_get_destpath","get_DestPath","get_DestPath method [COM+]","get_DestPath method [COM+]","IMessageMover interface"]
old-location: cos\imessagemover_get_destpath.htm
tech.root: cos
ms.assetid: 3adb24d5-b56d-4740-838b-d5b7571950e2
ms.date: 12/05/2018
ms.keywords: IMessageMover interface [COM+],get_DestPath method, IMessageMover.get_DestPath, IMessageMover::get_DestPath, comsvcs/IMessageMover::get_DestPath, cos.imessagemover_get_destpath, get_DestPath, get_DestPath method [COM+], get_DestPath method [COM+],IMessageMover interface
req.header: comsvcs.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMessageMover::get_DestPath
 - comsvcs/IMessageMover::get_DestPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMessageMover.get_DestPath
---

# IMessageMover::get_DestPath


## -description

Retrieves the path of the destination (output) queue.

## -parameters

### -param pVal [out]

The path.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imessagemover">IMessageMover</a>