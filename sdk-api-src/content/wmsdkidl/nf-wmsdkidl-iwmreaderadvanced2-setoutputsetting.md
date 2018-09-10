---
UID: NF:wmsdkidl.IWMReaderAdvanced2.SetOutputSetting
title: IWMReaderAdvanced2::SetOutputSetting
author: windows-sdk-content
description: The SetOutputSetting method specifies a named setting for a particular output.
old-location: wmformat\iwmreaderadvanced2_setoutputsetting.htm
tech.root: wmformat
ms.assetid: 035a74d2-288d-4754-8cb2-4508b7fe4649
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderAdvanced2 interface [windows Media Format],SetOutputSetting method, IWMReaderAdvanced2.SetOutputSetting, IWMReaderAdvanced2::SetOutputSetting, IWMReaderAdvanced2SetOutputSetting, SetOutputSetting, SetOutputSetting method [windows Media Format], SetOutputSetting method [windows Media Format],IWMReaderAdvanced2 interface, wmformat.iwmreaderadvanced2_setoutputsetting, wmsdkidl/IWMReaderAdvanced2::SetOutputSetting
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderAdvanced2.SetOutputSetting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced2::SetOutputSetting


## -description



The <b>SetOutputSetting</b> method specifies a named setting for a particular output.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param pszName [in]

Pointer to a wide-character null-terminated string containing the name. For a list of global constants that represent setting names, see <a href="https://msdn.microsoft.com/effe6c07-e6df-45b0-b865-2a025c466d6f">Output Settings</a>.


### -param Type [in]

Member of the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type that specifies the type of the value.


### -param pValue [in]

Pointer to a byte array containing the value.


### -param cbLength [in]

Size of <i>pValue</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/a46da973-8f2f-48b8-9a74-d54e67f68a83">IWMReaderAdvanced2::GetOutputSetting</a>
 

 

