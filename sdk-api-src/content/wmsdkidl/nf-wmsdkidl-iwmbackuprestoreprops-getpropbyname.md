---
UID: NF:wmsdkidl.IWMBackupRestoreProps.GetPropByName
title: IWMBackupRestoreProps::GetPropByName (wmsdkidl.h)
author: windows-sdk-content
description: The GetPropByName method retrieves the value of a property by name.
old-location: wmformat\iwmbackuprestoreprops_getpropbyname.htm
tech.root: wmformat
ms.assetid: 771a7a49-7d42-4537-9945-97b907404097
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPropByName, GetPropByName method [windows Media Format], GetPropByName method [windows Media Format],IWMBackupRestoreProps interface, IWMBackupRestoreProps interface [windows Media Format],GetPropByName method, IWMBackupRestoreProps.GetPropByName, IWMBackupRestoreProps::GetPropByName, IWMBackupRestorePropsGetPropByName, wmformat.iwmbackuprestoreprops_getpropbyname, wmsdkidl/IWMBackupRestoreProps::GetPropByName
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
 - IWMBackupRestoreProps.GetPropByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMBackupRestoreProps::GetPropByName


## -description


<p class="CCE_Message">[<b>GetPropByName</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>GetPropByName</b> method retrieves the value of a property by name.



This method is not implemented.
      


## -parameters




### -param pszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the name.


### -param pType [out]

Pointer to a variable containing one member of the <b>WMT_ATTR_DATATYPE</b> enumeration type.


### -param pValue [out]

Pointer to a byte array containing the value of the property.


### -param pcbLength [in, out]

On input, contains the length of <i>pValue</i>. On output, points to a count of the bytes in <i>pValue</i> that are used.


## -returns



The method returns E_NOTIMPL.




## -remarks



You should make two calls to <b>GetPropByName</b>. On the first call, pass <b>NULL</b> as <i>pValue</i>. On return, the value pointed to by <i>pcbLength</i> is set to the buffer size required to hold the property value. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop">IWMBackupRestoreProps::SetProp</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a>
 

 

