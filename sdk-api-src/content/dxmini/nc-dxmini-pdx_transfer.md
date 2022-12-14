---
UID: NC:dxmini.PDX_TRANSFER
title: PDX_TRANSFER (dxmini.h)
description: The DxTransfer callback function informs the driver to bus master data from a surface to the buffer specified in the memory descriptor list (MDL).
helpviewer_keywords: ["DxTransfer","DxTransfer callback function [Display Devices]","PDX_TRANSFER","PDX_TRANSFER callback","VideoMiniPort_DxApiFunctions_f6a3f689-7e04-4dec-850c-fa47b5ac1543.xml","display.dxtransfer","dxmini/DxTransfer"]
old-location: display\dxtransfer.htm
tech.root: display
ms.assetid: 62e1a5f6-9777-4acf-a531-b3554eaf89a6
ms.date: 12/05/2018
ms.keywords: DxTransfer, DxTransfer callback function [Display Devices], PDX_TRANSFER, PDX_TRANSFER callback, VideoMiniPort_DxApiFunctions_f6a3f689-7e04-4dec-850c-fa47b5ac1543.xml, display.dxtransfer, dxmini/DxTransfer
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Desktop
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDX_TRANSFER
 - dxmini/PDX_TRANSFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxmini.h
api_name:
 - DxTransfer
---

## -description

The<i> DxTransfer</i> callback function informs the driver to bus master data from a surface to the buffer specified in the memory descriptor list (MDL).

## -parameters

### -param unnamedParam1
Points to the miniport driver's device extension.

### -param unnamedParam2
Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddtransferininfo">DDTRANSFERININFO</a> structure that contains the transfer information for the surface.

### -param unnamedParam3
Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddtransferoutinfo">DDTRANSFEROUTINFO</a> structure that contains the polarity of the field being captured.

## -returns

<i>DxTransfer</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:

## -remarks

The MDL is defined in <a href="/windows-hardware/drivers/">WDM</a> documentation.

As shown in the following code sample, the video miniport driver can use the pointer to the MDL in the <b>lpDestMDL</b> member of the DDTRANSFERININFO structure at the <i>TransferInInfo</i> parameter to bus master data to the physical memory pages that make up a scattered buffer:

```cpp
DWORD 
DxTransfer(
    DEVICE_EXT *pDeviceExt, 
    PDDTRANSFERININFO pTransferInInfo, 
    PDDTRANSFEROUTINFO pTransferOutInfo
    )
{
    PMDL pMdl;
    UINT uiNbPages;
    PPFN_NUMBER pPages;
    PVOID MappedSystemVa;
    ULONG ByteCount;

    pMdl = pTransferInInfo->lpDestMDL;
    MappedSystemVa = MmGetMdlVirtualAddress(pMdl);
    ByteCount = MmGetMdlByteCount(pMdl);
    uiNbPages = ADDRESS_AND_SIZE_TO_SPAN_PAGES(MappedSystemVa,
                                               ByteCount);
    pPages = MmGetMdlPfnArray(pMdl)
    for (i=0; i<uiNbPages; i++) {
        //
        // Transfer to page[i]
        //
        pPages[i];
    }
}
```

See the <a href="/windows-hardware/drivers/kernel/mm-bad-pointer">ADDRESS_AND_SIZE_TO_SPAN_PAGES</a>, <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-mmgetmdlbytecount">MmGetMdlByteCount</a>, <a href="/windows-hardware/drivers/kernel/mm-bad-pointer">MmGetMdlPfnArray</a>, and <a href="/windows-hardware/drivers/kernel/mm-bad-pointer">MmGetMdlVirtualAddress</a> kernel-mode macros for more information.

<i>DxTransfer</i> is called at hardware interrupt time. This means the driver cannot wait for a previous bus master to complete and it cannot call any functions that are not safe to call at interrupt time (that is, most of them).

In addition, the driver should not fail the call just because the hardware is currently busy. Instead, the driver should maintain an internal queue.

## -see-also

<a href="/windows-hardware/drivers/kernel/mm-bad-pointer">ADDRESS_AND_SIZE_TO_SPAN_PAGES</a>

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddtransferininfo">DDTRANSFERININFO</a>

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddtransferoutinfo">DDTRANSFEROUTINFO</a>

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-mmgetmdlbytecount">MmGetMdlByteCount</a>

<a href="/windows-hardware/drivers/kernel/mm-bad-pointer">MmGetMdlPfnArray</a>

<a href="/windows-hardware/drivers/kernel/mm-bad-pointer">MmGetMdlVirtualAddress</a>
