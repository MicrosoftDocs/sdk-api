---
UID: NF:wia_xp.IEnumWIA_DEV_CAPS.Next
title: IEnumWIA_DEV_CAPS::Next
author: windows-sdk-content
description: The IEnumWIA_DEV_CAPS::Next method fills an array of pointers to WIA_DEV_CAP structures.
old-location: wia\_wia_IEnumWIA_DEV_CAPS_Next.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_dev_caps\next.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumWIA_DEV_CAPS interface [WIA],Next method, IEnumWIA_DEV_CAPS.Next, IEnumWIA_DEV_CAPS::Next, Next, Next method [WIA], Next method [WIA],IEnumWIA_DEV_CAPS interface, _wia_IEnumWIA_DEV_CAPS_Next, wia._wia_IEnumWIA_DEV_CAPS_Next, wia_xp/IEnumWIA_DEV_CAPS::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaguid.lib
 - Wiaguid.dll
api_name:
 - IEnumWIA_DEV_CAPS.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumWIA_DEV_CAPS::Next


## -description


The <b>IEnumWIA_DEV_CAPS::Next</b> method fills an array of pointers to <a href="https://msdn.microsoft.com/en-us/library/ms629872(v=VS.85).aspx">WIA_DEV_CAP</a> structures.



## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of array elements in the array indicated by the <i>rgelt</i> parameter.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms629872(v=VS.85).aspx">WIA_DEV_CAP</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms629872(v=VS.85).aspx">WIA_DEV_CAP</a> structures. <b>IEnumWIA_DEV_CAPS::Next</b> fills this array of structures.


### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

On output, this parameter contains the number of structure pointers actually stored in the array indicated by the <i>rgelt</i> parameter.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications use this method to query the capabilities of each available Windows Image Acquisition (WIA) hardware device. To do so, the application passes a pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms629872(v=VS.85).aspx">WIA_DEV_CAP</a> structures that it allocates. It also passes in the number of array elements in the parameter <i>celt</i>. The <b>IEnumWIA_DEV_CAPS::Next</b> method fills the array with structures. Applications then use the structures to enumerate WIA hardware device capabilities.

WIA device capabilities are defined as events and commands that the device supports. Using the <i>rgelt</i> array, <b>IEnumWIA_DEV_CAPS::Next</b> passes a single structure to the application for each event and command that the device supports.

Note that <b>IEnumWIA_DEV_CAPS::Next</b> dynamically allocates the <a href="https://msdn.microsoft.com/en-us/library/ms629872(v=VS.85).aspx">WIA_DEV_CAP</a> structures it provides to applications. Therefore, applications must delete the <b>WIA_DEV_CAP</b> structures they receive through the <i>rgelt</i> parameter. Applications should use <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the <i>bstrName</i>, <i>bstrDescription</i>, and <i>bstrIcon</i> fields of all <b>WIA_DEV_CAP</b> structures.



