---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IBrowserService2::_ExecChildren


## -description


Deprecated. Enables the derived class to issue a command through the <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a> method directly, instead of relying on the base class.


## -parameters




### -param punkBar [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the <a href="https://msdn.microsoft.com/5c8b455e-7740-4f71-aef6-27390a11a1a3">IOleCommandTarget</a> interface.


### -param fBroadcast [in]

Type: <b>BOOL</b>

<b>TRUE</b> to broadcast the command; <b>FALSE</b> otherwise.


### -param pguidCmdGroup [in]

Type: <b>const GUID*</b>

A pointer to the unique identifier of the command group; can be <b>NULL</b> to specify the standard group.


### -param nCmdID [in]

Type: <b>DWORD</b>

The command to be executed. This command must belong to the group specified with <i>pguidCmdGroup</i>.


### -param nCmdexecopt [in]

Type: <b>DWORD</b>

The values taken from the <a href="https://msdn.microsoft.com/6245725e-51d4-40e1-8cf1-a65657e790ef">OLECMDEXECOPT</a> enumeration, which describe how the object should execute the command.


### -param pvarargIn [in]

Type: <b>VARIANTARG*</b>

A pointer to a <b>VARIANTARG</b> structure containing input arguments. Can be <b>NULL</b>.


### -param pvarargOut [in, out]

Type: <b>VARIANTARG*</b>

A pointer to a <b>VARIANTARG</b> structure to receive command output. Can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For further information, see <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a>.



