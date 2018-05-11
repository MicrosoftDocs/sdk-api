---
UID: NF:msctf.ITfKeystrokeMgr.UnpreserveKey
title: ITfKeystrokeMgr::UnpreserveKey
author: windows-driver-content
description: ITfKeystrokeMgr::UnpreserveKey method
old-location: tsf\itfkeystrokemgr_unpreservekey.htm
old-project: TSF
ms.assetid: 05975fce-04c3-4316-a9b2-ed015e7aa8fe
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],UnpreserveKey method, ITfKeystrokeMgr.UnpreserveKey, ITfKeystrokeMgr::UnpreserveKey, UnpreserveKey, UnpreserveKey method [Text Services Framework], UnpreserveKey method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_unpreservekey_ref, msctf/ITfKeystrokeMgr::UnpreserveKey, tsf.itfkeystrokemgr_unpreservekey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfKeystrokeMgr.UnpreserveKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfKeystrokeMgr::UnpreserveKey


## -description




## -parameters




### -param rguid [in]

Contains the command GUID of the preserved key.


### -param pprekey [in]

Pointer to a <a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">TF_PRESERVEDKEY</a> structure that specifies the preserved key. The <i>uVKey</i> member contains the virtual key code and the <i>uModifiers</i> member identifies the modifiers of the preserved key.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The preserved key is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



Preserved keys are registered by TSF text services and provide keyboard shortcuts to common commands implemented by the TSF text service.




## -see-also




<a href="https://msdn.microsoft.com/93c1591d-2c95-45cb-8fc5-5726e905f202">ITfKeystrokeMgr</a>



<a href="https://msdn.microsoft.com/ad5cd485-9231-4c29-8977-754dbf25c979">ITfKeystrokeMgr::PreserveKey
      </a>



<a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">
        TF_PRESERVEDKEY
      </a>
 

 

