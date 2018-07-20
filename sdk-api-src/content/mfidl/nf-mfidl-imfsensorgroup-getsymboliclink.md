---
UID: NF:mfidl.IMFSensorGroup.GetSymbolicLink
title: IMFSensorGroup::GetSymbolicLink
author: windows-sdk-content
description: Gets the symbolic link name of the sensor group.
old-location: mf\imfsensorgroup_getsymboliclink.htm
old-project: medfound
ms.assetid: F71CFD47-6D44-4288-A70E-70040D19DB2D
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetSymbolicLink, GetSymbolicLink method [Media Foundation], GetSymbolicLink method [Media Foundation],IMFSensorGroup interface, IMFSensorGroup interface [Media Foundation],GetSymbolicLink method, IMFSensorGroup.GetSymbolicLink, IMFSensorGroup::GetSymbolicLink, mf.imfsensorgroup_getsymboliclink, mfidl/IMFSensorGroup::GetSymbolicLink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
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
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorGroup.GetSymbolicLink
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorGroup::GetSymbolicLink


## -description


Gets the symbolic link name of the sensor group.


## -parameters




### -param SymbolicLink [out]

Buffer of <i>cchSymbolicLink</i> characters where the symbolic link name will be written.  The buffer must be large enough to account for the null terminator.


### -param cchSymbolicLink [in]

Number of characters available in <i>SymbolicLink</i> buffer.


### -param pcchWritten [out]

Output parameter containing the number of characters written to <i>SymbolicLink</i>.  This includes the null terminator.  If <i>SymbolicLink</i> is null and <i>cchSymbolicLink</i> is 0, <i>pcchWritten</i> will contain the number of characters needed (including the null terminator) to store the symbolic link name.


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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">

                The buffer provided in the <i>SymbolicLink</i> parameter is not large enough to contain the symbolic link name, including the null terminator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">

                The sensor group has not been initialized.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a>
 

 

