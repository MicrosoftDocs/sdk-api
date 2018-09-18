---
UID: NF:shobjidl_core.IShellItemResources.EnumResources
title: IShellItemResources::EnumResources
author: windows-sdk-content
description: Gets a resource enumerator object.
old-location: shell\IShellItemResources_EnumResources.htm
tech.root: shell
ms.assetid: 29ac8ac9-4bd1-470c-885a-56f860d50a70
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EnumResources, EnumResources method [Windows Shell], EnumResources method [Windows Shell],IShellItemResources interface, IShellItemResources interface [Windows Shell],EnumResources method, IShellItemResources.EnumResources, IShellItemResources::EnumResources, _shell_IShellItemResources_EnumResources, shell.IShellItemResources_EnumResources, shobjidl_core/IShellItemResources::EnumResources
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
 - IShellItemResources.EnumResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItemResources::EnumResources


## -description


Gets a resource enumerator object.


## -parameters




### -param ppenumr [out]

Type: <b><a href="https://msdn.microsoft.com/28c645cf-8c69-49d7-a95f-ced6467ad682">IEnumResources</a>**</b>

The address of an <a href="https://msdn.microsoft.com/28c645cf-8c69-49d7-a95f-ced6467ad682">IEnumResources</a> interface pointer.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



