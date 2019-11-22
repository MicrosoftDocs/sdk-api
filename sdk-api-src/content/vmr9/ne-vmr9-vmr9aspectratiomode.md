---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0004_0001
title: VMR9AspectRatioMode (vmr9.h)

description: The VMR9AspectRatioMode enumeration type is used with the IVMRWindowlessControl9::GetAspectRatioMode and IVMRWindowlessControl9::SetAspectRatioMode methods to set and retrieve the aspect ratio mode (VMR-9 only).
old-location: dshow\vmr9aspectratiomode.htm
tech.root: DirectShow
ms.assetid: 745e7aad-a598-4be6-b28b-bb5969ef0c77

ms.date: 12/05/2018
ms.keywords: VMR9ARMode_LetterBox, VMR9ARMode_None, VMR9AspectRatioMode, VMR9AspectRatioMode , VMR9AspectRatioMode enumeration [DirectShow], VMR9AspectRatioModeEnumeration, dshow.vmr9aspectratiomode, vmr9/VMR9ARMode_LetterBox, vmr9/VMR9ARMode_None, vmr9/VMR9AspectRatioMode
ms.topic: enum
f1_keywords: 
 - "vmr9/VMR9AspectRatioMode"
dev_langs:
 - c++
req.header: vmr9.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9AspectRatioMode
targetos: Windows
req.typenames: VMR9AspectRatioMode
req.redist: 
ms.custom: 19H1
---

# VMR9AspectRatioMode enumeration


## -description



The <code>VMR9AspectRatioMode</code> enumeration type is used with the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getaspectratiomode">IVMRWindowlessControl9::GetAspectRatioMode</a> and <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode">IVMRWindowlessControl9::SetAspectRatioMode</a> methods to set and retrieve the aspect ratio mode (VMR-9 only).




## -enum-fields




### -field VMR9ARMode_None

Indicates that the VMR is not attempting to maintain the aspect ratio of the source video.


### -field VMR9ARMode_LetterBox

Indicates that the VMR will maintain the aspect ratio of the source video by letterboxing within the output rectangle.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
 

 

