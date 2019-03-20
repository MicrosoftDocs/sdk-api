---
UID: NF:winbio_adapter.WbioQuerySensorInterface
title: WbioQuerySensorInterface function (winbio_adapter.h)
author: windows-sdk-content
description: Retrieves a pointer to the WINBIO_SENSOR_INTERFACE structure for the sensor adapter.
old-location: secbiomet\wbioquerysensorinterface.htm
tech.root: SecBioMet
ms.assetid: 83ca38e1-3258-4676-bcdd-4876ec8f3ae1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WbioQuerySensorInterface, WbioQuerySensorInterface function [Windows Biometric Framework API], secbiomet.wbioquerysensorinterface, winbio_adapter/WbioQuerySensorInterface
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WbioQuerySensorInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WbioQuerySensorInterface function


## -description


Retrieves a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd401660(v=VS.85).aspx">WINBIO_SENSOR_INTERFACE</a> structure for the sensor adapter.


## -parameters




### -param SensorInterface [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd401660(v=VS.85).aspx">WINBIO_SENSOR_INTERFACE</a> structure.


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
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>SensorInterface</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The Windows Biometric Framework calls this function after loading a sensor adapter DLL into memory.
Every sensor adapter DLL must therefore implement and export the <a href="https://msdn.microsoft.com/d98da825-ce27-41ec-8f82-6f44e4854018">WbioQueryEngineInterface</a>  function. The function name is case-sensitive, and its spelling and signature must exactly match the description provided in the Syntax section.

To be visible to the Windows Biometric Framework, the <a href="https://msdn.microsoft.com/d98da825-ce27-41ec-8f82-6f44e4854018">WbioQueryEngineInterface</a> function must be named in the EXPORTS section of the export definition linker command file for the DLL.



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




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

