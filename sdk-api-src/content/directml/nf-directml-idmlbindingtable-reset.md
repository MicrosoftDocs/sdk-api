---
UID: NF:directml.IDMLBindingTable.Reset
title: IDMLBindingTable::Reset
description: Resets the binding table to wrap a new range of descriptors, potentially for a different operator or initializer. This allows dynamic reuse of the binding table.
helpviewer_keywords: ["IDMLBindingTable interface","Reset method","IDMLBindingTable.Reset","IDMLBindingTable::Reset","Reset","Reset method","Reset method","IDMLBindingTable interface","direct3d12.idmlbindingtable_reset","directml/IDMLBindingTable::Reset"]
old-location: direct3d12\idmlbindingtable_reset.htm
tech.root: directml
ms.assetid: 85A816F8-CD3A-43B0-B63C-C58BC47438B1
ms.date: 12/5/2018
ms.keywords: IDMLBindingTable interface,Reset method, IDMLBindingTable.Reset, IDMLBindingTable::Reset, Reset, Reset method, Reset method,IDMLBindingTable interface, direct3d12.idmlbindingtable_reset, directml/IDMLBindingTable::Reset
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
 - IDMLBindingTable::Reset
 - directml/IDMLBindingTable::Reset
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
 - IDMLBindingTable.Reset
---

# IDMLBindingTable::Reset


## -description

Resets the binding table to wrap a new range of descriptors, potentially for a different operator or
        initializer. This allows dynamic reuse of the binding table.

Resetting a binding table doesn't modify any previous bindings created by the table. Because of this, it is
        safe to reset the binding table immediately after supplying it to [IDMLCommandRecorder::RecordDispatch](/windows/win32/api/directml/nf-directml-idmlcommandrecorder-recorddispatch), even if that work has not yet completed execution on the GPU, so long as the
        underlying descriptors remain valid.

See [IDMLDevice::CreateBindingTable](/windows/win32/api/directml/nf-directml-idmldevice-createbindingtable) for more information on the parameters supplied to this method.

## -parameters

### -param desc [in, optional]

Type: <b>const [DML_BINDING_TABLE_DESC](/windows/win32/api/directml/ns-directml-dml_binding_table_desc)*</b>

An optional pointer to a [DML_BINDING_TABLE_DESC](/windows/win32/api/directml/ns-directml-dml_binding_table_desc) containing the binding table parameters. This may be <b>nullptr</b>, indicating an empty binding table.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>

[IDMLBindingTable](/windows/win32/api/directml/nn-directml-idmlbindingtable)
