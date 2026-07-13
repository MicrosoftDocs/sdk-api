---
UID: NF:winbio_adapter.WbioQueryEngineInterface
title: WbioQueryEngineInterface function (winbio_adapter.h)
description: Retrieves a pointer to the WINBIO_ENGINE_INTERFACE structure for the engine adapter.
helpviewer_keywords: ["WbioQueryEngineInterface","WbioQueryEngineInterface function [Windows Biometric Framework API]","secbiomet.wbioqueryengineinterface","winbio_adapter/WbioQueryEngineInterface"]
old-location: secbiomet\wbioqueryengineinterface.htm
tech.root: SecBioMet
ms.assetid: d98da825-ce27-41ec-8f82-6f44e4854018
ms.date: 12/05/2018
ms.keywords: WbioQueryEngineInterface, WbioQueryEngineInterface function [Windows Biometric Framework API], secbiomet.wbioqueryengineinterface, winbio_adapter/WbioQueryEngineInterface
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
 - WbioQueryEngineInterface
 - winbio_adapter/WbioQueryEngineInterface
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
 - WbioQueryEngineInterface
---

# WbioQueryEngineInterface function


## -description

Retrieves a pointer to the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_engine_interface">WINBIO_ENGINE_INTERFACE</a> structure for the engine adapter.

## -parameters

### -param EngineInterface [out]

Address of a variable that receives a pointer to the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_engine_interface">WINBIO_ENGINE_INTERFACE</a> structure.

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
The <i>EngineInterface</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The Windows Biometric Framework calls this function after loading an engine adapter DLL into memory.
Every engine adapter DLL must therefore implement and export the <b>WbioQueryEngineInterface</b>  function. The function name is case-sensitive, and its spelling and signature must exactly match that  provided in the Syntax section.

To be visible to the Windows Biometric Framework, the <b>WbioQueryEngineInterface</b> function must be named in the EXPORTS section of the export definition linker command file for the DLL.



#### Examples

The following pseudocode shows one possible implementation of this function. 


```cpp
HRESULT
WINAPI
WbioQueryEngineInterface(
    __out PWINBIO_ENGINE_INTERFACE *EngineInterface)
{
    // g_EngineInterface is a global variable.
    *EngineInterface = &g_EngineInterface;
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>