---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetOutputSetting
title: IWMReaderAdvanced2::GetOutputSetting
author: windows-sdk-content
description: The GetOutputSetting method retrieves a setting for a particular output by name.
old-location: wmformat\iwmreaderadvanced2_getoutputsetting.htm
old-project: wmformat
ms.assetid: a46da973-8f2f-48b8-9a74-d54e67f68a83
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetOutputSetting, GetOutputSetting method [windows Media Format], GetOutputSetting method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetOutputSetting method, IWMReaderAdvanced2.GetOutputSetting, IWMReaderAdvanced2::GetOutputSetting, IWMReaderAdvanced2GetOutputSetting, wmformat.iwmreaderadvanced2_getoutputsetting, wmsdkidl/IWMReaderAdvanced2::GetOutputSetting
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMReaderAdvanced2.GetOutputSetting
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced2::GetOutputSetting


## -description



The <b>GetOutputSetting</b> method retrieves a setting for a particular output by name.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param pszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the setting name. For a list of global constants representing setting names, see <a href="https://msdn.microsoft.com/effe6c07-e6df-45b0-b865-2a025c466d6f">Output Settings</a>.


### -param pType [out]

Pointer to a member of the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type that specifies the type of the value.


### -param pValue [out]

Pointer to a byte buffer containing the value. Pass <b>NULL</b> to retrieve the length of the buffer required.


### -param pcbLength [in, out]

On input, pointer to a variable containing the length of <i>pValue</i>. On output, the variable contains the number of bytes in <i>pValue</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



You should make two calls to <b>GetOutputSetting</b>. On the first call, pass <b>NULL</b> for <i>pValue</i>. On return, the value pointed to by <i>pcbLength</i> is set to the buffer size required to hold the setting value. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.




## -see-also




<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>
 

 

