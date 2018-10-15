---
UID: NF:shobjidl_core.IEnumFullIDList.Skip
title: IEnumFullIDList::Skip
author: windows-sdk-content
description: Skips a specified number of IDLIST_ABSOLUTE items.
old-location: shell\IEnumFullIDList_Skip.htm
tech.root: shell
ms.assetid: f47bdab1-57be-4f40-a142-ad5edcf6fbfd
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IEnumFullIDList interface [Windows Shell],Skip method, IEnumFullIDList.Skip, IEnumFullIDList::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],IEnumFullIDList interface, _shell_IEnumFullIDList_Skip, shell.IEnumFullIDList_Skip, shobjidl_core/IEnumFullIDList::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IEnumFullIDList.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumFullIDList::Skip


## -description


Skips a specified number of IDLIST_ABSOLUTE  items.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of items to skip.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The enumeration index is advanced by the number of items skipped.



