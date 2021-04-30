---
UID: NF:directml.IDMLDevice.CreateCommandRecorder
title: IDMLDevice::CreateCommandRecorder
description: Creates a DirectML command recorder.
helpviewer_keywords: ["CreateCommandRecorder","CreateCommandRecorder method","CreateCommandRecorder method","IDMLDevice interface","IDMLDevice interface","CreateCommandRecorder method","IDMLDevice.CreateCommandRecorder","IDMLDevice::CreateCommandRecorder","direct3d12.idmldevice_createcommandrecorder","directml/IDMLDevice::CreateCommandRecorder"]
old-location: direct3d12\idmldevice_createcommandrecorder.htm
tech.root: directml
ms.assetid: 95A70E8B-6C39-422B-91A6-1660E7E05D4C
ms.date: 12/5/2018
ms.keywords: CreateCommandRecorder, CreateCommandRecorder method, CreateCommandRecorder method,IDMLDevice interface, IDMLDevice interface,CreateCommandRecorder method, IDMLDevice.CreateCommandRecorder, IDMLDevice::CreateCommandRecorder, direct3d12.idmldevice_createcommandrecorder, directml/IDMLDevice::CreateCommandRecorder
req.header: directml.h
req.include-header: 
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMLDevice::CreateCommandRecorder
 - directml/IDMLDevice::CreateCommandRecorder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.dll
api_name:
 - IDMLDevice.CreateCommandRecorder
---

# IDMLDevice::CreateCommandRecorder


## -description

Creates a DirectML command recorder.

A command recorder allows your application to record the initialization and execution of compiled operators into
        existing Direct3D 12 command lists. The command recorder is a stateless object: it does not own command lists or
        operators, nor does it execute any GPU work. Instead, it merely records the commands necessary for
        dispatching initialization or execution into an application-supplied command list. Your application is then
        responsible for submitting the execution of that command list to the Direct3D 12 command queue.

## -parameters

### -param riid

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>. This is expected to be the GUID of [IDMLCommandRecorder](/windows/win32/api/directml/nn-directml-idmlcommandrecorder).

### -param ppv [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the command recorder. This is the address of a pointer to an [IDMLCommandRecorder](/windows/win32/api/directml/nn-directml-idmlcommandrecorder), representing  the command recorder created.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)
