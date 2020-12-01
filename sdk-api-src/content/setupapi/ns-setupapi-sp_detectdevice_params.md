---
UID: NS:setupapi._SP_DETECTDEVICE_PARAMS
title: SP_DETECTDEVICE_PARAMS (setupapi.h)
description: An SP_DETECTDEVICE_PARAMS structure corresponds to a DIF_DETECT installation request.
helpviewer_keywords: ["*PSP_DETECTDEVICE_PARAMS","PSP_DETECTDEVICE_PARAMS","PSP_DETECTDEVICE_PARAMS structure pointer [Device and Driver Installation]","SP_DETECTDEVICE_PARAMS","SP_DETECTDEVICE_PARAMS structure [Device and Driver Installation]","devinst.sp_detectdevice_params","di-struct_6de1fd38-be9a-42e6-ae10-5825aef12880.xml","setupapi/PSP_DETECTDEVICE_PARAMS","setupapi/SP_DETECTDEVICE_PARAMS"]
old-location: devinst\sp_detectdevice_params.htm
tech.root: devinst
ms.assetid: 77682651-217f-4e3a-9d0e-0a93d315de53
ms.date: 12/05/2018
ms.keywords: '*PSP_DETECTDEVICE_PARAMS, PSP_DETECTDEVICE_PARAMS, PSP_DETECTDEVICE_PARAMS structure pointer [Device and Driver Installation], SP_DETECTDEVICE_PARAMS, SP_DETECTDEVICE_PARAMS structure [Device and Driver Installation], devinst.sp_detectdevice_params, di-struct_6de1fd38-be9a-42e6-ae10-5825aef12880.xml, setupapi/PSP_DETECTDEVICE_PARAMS, setupapi/SP_DETECTDEVICE_PARAMS'
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SP_DETECTDEVICE_PARAMS, *PSP_DETECTDEVICE_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_DETECTDEVICE_PARAMS
 - setupapi/_SP_DETECTDEVICE_PARAMS
 - PSP_DETECTDEVICE_PARAMS
 - setupapi/PSP_DETECTDEVICE_PARAMS
 - SP_DETECTDEVICE_PARAMS
 - setupapi/SP_DETECTDEVICE_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DETECTDEVICE_PARAMS
---

# SP_DETECTDEVICE_PARAMS structure


## -description

An SP_DETECTDEVICE_PARAMS structure corresponds to a DIF_DETECT installation request.

## -struct-fields

### -field ClassInstallHeader

An install request header that contains the size of the header and the DIF code for the request. See <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>.

### -field DetectProgressNotify

A callback routine that displays a progress bar for the device detection operation. The callback routine is supplied by the <a href="/windows-hardware/drivers/install/system-provided-device-installation-components">device installation component</a> that sends the <a href="/windows-hardware/drivers/install/dif-detect">DIF_DETECT</a> request. The callback has the following prototype:


```
typedef BOOL (CALLBACK* PDETECT_PROGRESS_NOTIFY)(
    IN PVOID ProgressNotifyParam,
    IN DWORD DetectComplete
    );
```


<i>ProgressNotifyParam</i> is an opaque "handle" that identifies the detection operation. This value is supplied by the <a href="/windows-hardware/drivers/install/system-provided-device-installation-components">device installation component</a> that sent the DIF_DETECT request. 

<i>DetectComplete</i> is a value between 0 and 100 that indicates the percent completion. The class installer increments this value at various stages of its detection activities, to notify the user of its progress.

### -field ProgressNotifyParam

The opaque <b>ProgressNotifyParam</b> "handle" that the class installer passes to the progress callback routine.

## -see-also

<a href="/windows-hardware/drivers/install/dif-detect">DIF_DETECT</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>