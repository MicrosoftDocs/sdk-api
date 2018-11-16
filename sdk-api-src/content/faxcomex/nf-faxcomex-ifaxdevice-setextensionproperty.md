---
UID: NF:faxcomex.IFaxDevice.SetExtensionProperty
title: IFaxDevice::SetExtensionProperty
author: windows-sdk-content
description: The IFaxDevice::SetExtensionProperty method stores an extension configuration property at the device level.
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_setextensionproperty_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5szd.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxDevice interface [Fax Service],SetExtensionProperty method, IFaxDevice.SetExtensionProperty, IFaxDevice::SetExtensionProperty, SetExtensionProperty, SetExtensionProperty method [Fax Service], SetExtensionProperty method [Fax Service],IFaxDevice interface, _mfax_faxdevice.setextensionproperty, fax._mfax_faxdevice_cpp_mfax_faxdevice_setextensionproperty_cpp, fax._mfax_faxdevice_setextensionproperty, faxcomex/IFaxDevice::SetExtensionProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxDevice.SetExtensionProperty
 - IFaxDevice.SetExtensionProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxDevice.SetExtensionProperty
: 
---

# IFaxDevice::SetExtensionProperty


## -description


The <b>IFaxDevice::SetExtensionProperty</b> method stores an extension configuration property at the device level.


## -parameters




### -param bstrGUID [in]

Type: <b>BSTR</b>

Specifies a string GUID that identifies the data to set.


### -param vProperty [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies the data to be stored.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.

<div class="alert"><b>Note</b>  The required data is a blob of bytes represented as a variant safe array of unsigned chars (VT_UI1 | VT_ARRAY). The data is relevant only to the specific extension that uses it. For more information see <a href="https://msdn.microsoft.com/846f307f-f2ec-4edd-8ada-cb2199dcfed5">About the Fax Extension Configuration API</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a>



<a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a>



<a href="https://msdn.microsoft.com/e9800209-9ff9-495d-ab60-a0cee64eb569">Visual Basic Example</a>
 

 

