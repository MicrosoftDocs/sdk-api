---
UID: NF:wia_xp.IEnumWIA_DEV_INFO.Next
title: IEnumWIA_DEV_INFO::Next (wia_xp.h)
description: The IEnumWIA_DEV_INFO::Next method fills an array of pointers to IWiaPropertyStorage interfaces.
helpviewer_keywords: ["IEnumWIA_DEV_INFO interface [WIA]","Next method","IEnumWIA_DEV_INFO.Next","IEnumWIA_DEV_INFO::Next","Next","Next method [WIA]","Next method [WIA]","IEnumWIA_DEV_INFO interface","_wia_IEnumWIA_DEV_INFO_Next","wia._wia_IEnumWIA_DEV_INFO_Next","wia_xp/IEnumWIA_DEV_INFO::Next"]
old-location: wia\_wia_IEnumWIA_DEV_INFO_Next.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_dev_info\next.htm
ms.date: 12/05/2018
ms.keywords: IEnumWIA_DEV_INFO interface [WIA],Next method, IEnumWIA_DEV_INFO.Next, IEnumWIA_DEV_INFO::Next, Next, Next method [WIA], Next method [WIA],IEnumWIA_DEV_INFO interface, _wia_IEnumWIA_DEV_INFO_Next, wia._wia_IEnumWIA_DEV_INFO_Next, wia_xp/IEnumWIA_DEV_INFO::Next
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumWIA_DEV_INFO::Next
 - wia_xp/IEnumWIA_DEV_INFO::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaguid.lib
 - Wiaguid.dll
api_name:
 - IEnumWIA_DEV_INFO.Next
archived: true
---

# IEnumWIA_DEV_INFO::Next


## -description

The <b>IEnumWIA_DEV_INFO::Next</b> method fills an array of pointers to <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage">IWiaPropertyStorage</a> interfaces.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of array elements in the array indicated by the <i>rgelt</i> parameter.

### -param rgelt [out]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage">IWiaPropertyStorage</a>**</b>

Receives the address of an array of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage">IWiaPropertyStorage</a> interface pointers. <b>IEnumWIA_DEV_INFO::Next</b> fills this array with interface pointers.

### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

On output, this parameter contains the number of interface pointers actually stored in the array indicated by the <i>rgelt</i> parameter.

## -returns

Type: <b>HRESULT</b>

While there are devices left to enumerate, this method returns S_OK. It returns S_FALSE when the enumeration is finished. If the method fails, it returns a standard COM error code.

## -remarks

Applications use this method to query the properties of each available Windows Image Acquisition (WIA) hardware device. To do so, the application passes an array of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage">IWiaPropertyStorage</a> interface pointers that it allocates. It also passes the number of array elements in the parameter <i>celt</i>. The <b>IEnumWIA_DEV_INFO::Next</b> method fills the array with pointers to <b>IWiaPropertyStorage</b> interfaces. Applications can query the interfaces for the properties that the device supports.

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the interface pointers they receive through the <i>rgelt</i> parameter.