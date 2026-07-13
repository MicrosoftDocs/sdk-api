---
UID: NF:winbio_adapter.WbioQueryStorageInterface
title: WbioQueryStorageInterface function (winbio_adapter.h)
description: Retrieves a pointer to the WINBIO_STORAGE_INTERFACE structure for the storage adapter.
helpviewer_keywords: ["WbioQueryStorageInterface","WbioQueryStorageInterface function [Windows Biometric Framework API]","secbiomet.wbioquerystorageinterface","winbio_adapter/WbioQueryStorageInterface"]
old-location: secbiomet\wbioquerystorageinterface.htm
tech.root: SecBioMet
ms.assetid: ff7297ee-8d0a-41f4-8abf-66ab5163dae7
ms.date: 12/05/2018
ms.keywords: WbioQueryStorageInterface, WbioQueryStorageInterface function [Windows Biometric Framework API], secbiomet.wbioquerystorageinterface, winbio_adapter/WbioQueryStorageInterface
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WbioQueryStorageInterface
 - winbio_adapter/WbioQueryStorageInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WbioQueryStorageInterface
---

# WbioQueryStorageInterface function


## -description

Retrieves a pointer to the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_storage_interface">WINBIO_STORAGE_INTERFACE</a> structure for the storage adapter.

## -parameters

### -param StorageInterface [out]

Address of a variable that receives a pointer to the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_storage_interface">WINBIO_STORAGE_INTERFACE</a> structure.

## -returns

If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>StorageInterface</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The Windows Biometric Framework calls this function after loading a storage adapter DLL into memory.
Every storage adapter DLL must therefore implement and export the <b>WbioQueryStorageInterface</b>  function. The function name is case-sensitive, and its spelling and signature must exactly match that provided in the Syntax section.

To be visible to the Windows Biometric Framework, the <b>WbioQueryStorageInterface</b> function must be named in the EXPORTS section of the export definition linker command file for the DLL.



#### Examples

The following pseudocode shows one possible implementation of this function.


```cpp
HRESULT
WINAPI
WbioQueryStorageInterface(
    __out PWINBIO_STORAGE_INTERFACE *StorageInterface
    )
{
    *StorageInterface = &g_StorageInterface; 
    return S_OK;
}
```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>