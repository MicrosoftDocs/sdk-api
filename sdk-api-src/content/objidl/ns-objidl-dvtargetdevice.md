---
UID: NS:objidl.tagDVTARGETDEVICE
title: DVTARGETDEVICE (objidl.h)
description: Specifies information about the target device for which data is being composed. DVTARGETDEVICE contains enough information about a Windows target device so a handle to a device context (HDC) can be created using the CreateDC function.
helpviewer_keywords: ["DVTARGETDEVICE","DVTARGETDEVICE structure [COM]","_ole_DVTARGETDEVICE","com.dvtargetdevice","objidl/DVTARGETDEVICE"]
old-location: com\dvtargetdevice.htm
tech.root: com
ms.assetid: 724ff714-c170-4d06-92cb-e042e41c0af2
ms.date: 12/05/2018
ms.keywords: DVTARGETDEVICE, DVTARGETDEVICE structure [COM], _ole_DVTARGETDEVICE, com.dvtargetdevice, objidl/DVTARGETDEVICE
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: DVTARGETDEVICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVTARGETDEVICE
 - objidl/tagDVTARGETDEVICE
 - DVTARGETDEVICE
 - objidl/DVTARGETDEVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ObjIdl.h
api_name:
 - DVTARGETDEVICE
---

# DVTARGETDEVICE structure


## -description

Specifies information about the target device for which data is being composed. <b>DVTARGETDEVICE</b> contains enough information about a Windows target device so a handle to a device context (<b>HDC</b>) can be created using the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a> function.

## -struct-fields

### -field tdSize

The size, in bytes, of the <b>DVTARGETDEVICE</b> structure. The initial size is included so the structure can be copied more easily.

### -field tdDriverNameOffset

The offset, in bytes, from the beginning of the structure to the device driver name, which is stored as a NULL-terminated string in the <b>tdData</b> buffer.

### -field tdDeviceNameOffset

The offset, in bytes, from the beginning of the structure to the device name, which is stored as a NULL-terminated string in the <b>tdData</b> buffer. This value can be zero to indicate no device name.

### -field tdPortNameOffset

The offset, in bytes, from the beginning of the structure to the port name, which is stored as a NULL-terminated string in the <b>tdData</b> buffer. This value can be zero to indicate no port name.

### -field tdExtDevmodeOffset

The offset, in bytes, from the beginning of the structure to the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure retrieved by calling <a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a>.

### -field tdData

An array of bytes containing data for the target device. It is not necessary to include empty strings in <b>tdData</b> (for names where the offset value is zero).

## -remarks

Some OLE 1 client applications incorrectly construct target devices by allocating too few bytes in the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure for the <b>DVTARGETDEVICE</b>. They typically only supply the number of bytes in the <b>dmSize</b> member of <b>DEVMODE</b>. The number of bytes to be allocated should be the sum of <b>dmSize</b> + <b>dmDriverExtra</b>. When a call is made to the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a> function with an incorrect target device, the printer driver tries to access the additional bytes and unpredictable results can occur. To help protect against a crash and make the additional bytes available, OLE pads the size of OLE 2 target devices created from OLE 1 target devices.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertolestreamtoistorage">OleConvertOLESTREAMToIStorage</a>