---
UID: NC:dxmini.PDX_TRANSFER
title: PDX_TRANSFER
author: windows-sdk-content
description: The DxTransfer callback function informs the driver to bus master data from a surface to the buffer specified in the memory descriptor list (MDL).
old-location: display\dxtransfer.htm
tech.root: display
ms.assetid: 62e1a5f6-9777-4acf-a531-b3554eaf89a6
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DxTransfer, DxTransfer callback function [Display Devices], PDX_TRANSFER, PDX_TRANSFER callback, VideoMiniPort_DxApiFunctions_f6a3f689-7e04-4dec-850c-fa47b5ac1543.xml, display.dxtransfer, dxmini/DxTransfer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxmini.h
api_name:
 - DxTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDX_TRANSFER callback function


## -description


The<i> DxTransfer</i> callback function informs the driver to bus master data from a surface to the buffer specified in the memory descriptor list (MDL).


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - TransferInInfo

Points to a <a href="https://msdn.microsoft.com/9e5f938d-0db6-4df6-a9c2-49840fef8c03">DDTRANSFERININFO</a> structure that contains the transfer information for the surface.


#### - TransferOutInfo

Points to a <a href="https://msdn.microsoft.com/0c029912-0540-438a-a255-aeb1a58ad275">DDTRANSFEROUTINFO</a> structure that contains the polarity of the field being captured.


## -returns



<i>DxTransfer</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The MDL is defined in <a href="https://msdn.microsoft.com/f10a63ab-2117-4a61-b3a2-cfbbe2d20d7c">WDM</a> documentation.

As shown in the following code sample, the video miniport driver can use the pointer to the MDL in the <b>lpDestMDL</b> member of the DDTRANSFERININFO structure at the <i>TransferInInfo</i> parameter to bus master data to the physical memory pages that make up a scattered buffer:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>DWORD 
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

    pMdl = pTransferInInfo-&gt;lpDestMDL;
    MappedSystemVa = MmGetMdlVirtualAddress(pMdl);
    ByteCount = MmGetMdlByteCount(pMdl);
    uiNbPages = ADDRESS_AND_SIZE_TO_SPAN_PAGES(MappedSystemVa,
                                               ByteCount);
    pPages = MmGetMdlPfnArray(pMdl)
    for (i=0; i&lt;uiNbPages; i++) {
        //
        // Transfer to page[i]
        //
        pPages[i];
    }
}</pre>
</td>
</tr>
</table></span></div>
See the <a href="https://msdn.microsoft.com/library/Ff540562(v=VS.85).aspx">ADDRESS_AND_SIZE_TO_SPAN_PAGES</a>, <a href="https://msdn.microsoft.com/a0493418-2ce2-4917-bf9f-e4dc726a3847">MmGetMdlByteCount</a>, <a href="https://msdn.microsoft.com/library/Ff554537(v=VS.85).aspx">MmGetMdlPfnArray</a>, and <a href="https://msdn.microsoft.com/library/Ff554539(v=VS.85).aspx">MmGetMdlVirtualAddress</a> kernel-mode macros for more information.

<i>DxTransfer</i> is called at hardware interrupt time. This means the driver cannot wait for a previous bus master to complete and it cannot call any functions that are not safe to call at interrupt time (that is, most of them).

In addition, the driver should not fail the call just because the hardware is currently busy. Instead, the driver should maintain an internal queue.




## -see-also




<a href="https://msdn.microsoft.com/library/Ff540562(v=VS.85).aspx">ADDRESS_AND_SIZE_TO_SPAN_PAGES</a>



<a href="https://msdn.microsoft.com/9e5f938d-0db6-4df6-a9c2-49840fef8c03">DDTRANSFERININFO</a>



<a href="https://msdn.microsoft.com/0c029912-0540-438a-a255-aeb1a58ad275">DDTRANSFEROUTINFO</a>



<a href="https://msdn.microsoft.com/a0493418-2ce2-4917-bf9f-e4dc726a3847">MmGetMdlByteCount</a>



<a href="https://msdn.microsoft.com/library/Ff554537(v=VS.85).aspx">MmGetMdlPfnArray</a>



<a href="https://msdn.microsoft.com/library/Ff554539(v=VS.85).aspx">MmGetMdlVirtualAddress</a>
 

 

