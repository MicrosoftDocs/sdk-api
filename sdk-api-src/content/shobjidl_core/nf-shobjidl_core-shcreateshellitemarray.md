---
UID: NF:shobjidl_core.SHCreateShellItemArray
title: SHCreateShellItemArray function
author: windows-driver-content
description: Creates a Shell item array object.
old-location: shell\SHCreateShellItemArray.htm
old-project: shell
ms.assetid: 024ccbc7-97f1-4cb5-8588-9c9b1f747336
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: SHCreateShellItemArray, SHCreateShellItemArray function [Windows Shell], _shell_SHCreateShellItemArray, shell.SHCreateShellItemArray, shobjidl_core/SHCreateShellItemArray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	SHCreateShellItemArray
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHCreateShellItemArray function


## -description


Creates a Shell item array object.


## -parameters




### -param pidlParent [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The ID list of the parent folder of the items specified in <i>ppidl</i>. If <i>psf</i> is specified, this parameter can be <b>NULL</b>. If this <i>pidlParent</i> is not specified, it is computed from the <i>psf</i> parameter using <a href="https://msdn.microsoft.com/3deb3467-b6f2-49f9-ba24-fd2cca80f247">IPersistFolder2</a>.


### -param psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

The Shell data source object that is the parent of the child items specified in <i>ppidl</i>. If <i>pidlParent</i> is specified, this parameter can be <b>NULL</b>.


### -param cidl [in]

Type: <b>UINT</b>

The number of elements in the array specified by <i>ppidl</i>.


### -param ppidl [in]

Type: <b>PCUITEMID_CHILD_ARRAY</b>

The list of child item IDs for which the array is being created. This value can be <b>NULL</b>.


### -param ppsiItemArray [out]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>**</b>

When this function returns, contains the address of an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



