---
UID: NF:winbio_adapter.WbioQuerySensorInterface
title: WbioQuerySensorInterface function (winbio_adapter.h)
description: Retrieves a pointer to the WINBIO_SENSOR_INTERFACE structure for the sensor adapter.
helpviewer_keywords: ["WbioQuerySensorInterface","WbioQuerySensorInterface function [Windows Biometric Framework API]","secbiomet.wbioquerysensorinterface","winbio_adapter/WbioQuerySensorInterface"]
old-location: secbiomet\wbioquerysensorinterface.htm
tech.root: SecBioMet
ms.assetid: 83ca38e1-3258-4676-bcdd-4876ec8f3ae1
ms.date: 12/05/2018
ms.keywords: WbioQuerySensorInterface, WbioQuerySensorInterface function [Windows Biometric Framework API], secbiomet.wbioquerysensorinterface, winbio_adapter/WbioQuerySensorInterface
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
 - WbioQuerySensorInterface
 - winbio_adapter/WbioQuerySensorInterface
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
 - WbioQuerySensorInterface
---

# WbioQuerySensorInterface function


## -description

Retrieves a pointer to the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_sensor_interface">WINBIO_SENSOR_INTERFACE</a> structure for the sensor adapter.

## -parameters

### -param SensorInterface [out]

Address of a variable that receives a pointer to the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_sensor_interface">WINBIO_SENSOR_INTERFACE</a> structure.

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
The <i>SensorInterface</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The Windows Biometric Framework calls this function after loading a sensor adapter DLL into memory.
Every sensor adapter DLL must therefore implement and export the <a href="/windows/desktop/api/winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface">WbioQueryEngineInterface</a>  function. The function name is case-sensitive, and its spelling and signature must exactly match the description provided in the Syntax section.

To be visible to the Windows Biometric Framework, the <a href="/windows/desktop/api/winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface">WbioQueryEngineInterface</a> function must be named in the EXPORTS section of the export definition linker command file for the DLL.



#### Examples

The following pseudocode shows one possible implementation of this function.


```cpp
HRESULT
WINAPI
WbioQuerySensorInterface(
    __out PWINBIO_SENSOR_INTERFACE *SensorInterface
    )
{
    // g_SensorInterface is a global variable.
    *SensorInterface = &g_SensorInterface;
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>