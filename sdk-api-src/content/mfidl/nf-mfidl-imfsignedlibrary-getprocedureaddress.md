---
UID: NF:mfidl.IMFSignedLibrary.GetProcedureAddress
title: IMFSignedLibrary::GetProcedureAddress
author: windows-sdk-content
description: Gets the procedure address of the specified function in the signed library.
old-location: mf\imfsignedlibrary_getprocedureaddress.htm
old-project: medfound
ms.assetid: d32678b0-422d-4fe8-9bbc-fc203a39fdd5
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetProcedureAddress, GetProcedureAddress method [Media Foundation], GetProcedureAddress method [Media Foundation],IMFSignedLibrary interface, IMFSignedLibrary interface [Media Foundation],GetProcedureAddress method, IMFSignedLibrary.GetProcedureAddress, IMFSignedLibrary::GetProcedureAddress, mf.imfsignedlibrary_getprocedureaddress, mfidl/IMFSignedLibrary::GetProcedureAddress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSignedLibrary.GetProcedureAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSignedLibrary::GetProcedureAddress


## -description


Gets the procedure address of the specified function in the signed library.


## -parameters




### -param name

The entry point name in the DLL that specifies the function.


### -param address

Receives the address of the entry point.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



See  <a href="https://msdn.microsoft.com/979A5FE5-0DED-4C5A-A27D-CDD10A4A8D5C">MFLoadSignedLibrary</a> for an example of how to create an <a href="https://msdn.microsoft.com/1170fd74-7da4-49a8-b095-dd1572db382d">IMFSignedLibrary</a> object and call the <b>GetProcedureAddress</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1170fd74-7da4-49a8-b095-dd1572db382d">IMFSignedLibrary</a>



<a href="https://msdn.microsoft.com/979A5FE5-0DED-4C5A-A27D-CDD10A4A8D5C">MFLoadSignedLibrary</a>
 

 

