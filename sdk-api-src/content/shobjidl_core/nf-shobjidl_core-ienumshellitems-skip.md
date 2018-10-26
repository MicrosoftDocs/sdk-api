---
UID: NF:shobjidl_core.IEnumShellItems.Skip
title: IEnumShellItems::Skip
author: windows-sdk-content
description: Skips a given number of IShellItem interfaces in the enumeration. Used when retrieving interfaces.
old-location: shell\IEnumShellItems_Skip.htm
tech.root: shell
ms.assetid: 5359c9d2-715a-4949-8f40-a35d04423dba
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IEnumShellItems interface [Windows Shell],Skip method, IEnumShellItems.Skip, IEnumShellItems::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],IEnumShellItems interface, _shell_IEnumShellItems_Skip, shell.IEnumShellItems_Skip, shobjidl_core/IEnumShellItems::Skip
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
 - IEnumShellItems.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumShellItems::Skip


## -description


Skips a given number of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces in the enumeration. Used when retrieving interfaces.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces to skip.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

