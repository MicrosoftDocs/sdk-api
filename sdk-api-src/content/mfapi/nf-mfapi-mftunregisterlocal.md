---
UID: NF:mfapi.MFTUnregisterLocal
title: MFTUnregisterLocal function
author: windows-sdk-content
description: Unregisters one or more Media Foundation transforms (MFTs) from the caller's process.
old-location: mf\mftunregisterlocal.htm
old-project: medfound
ms.assetid: e77edce7-0abb-41a3-a65e-fd159173e135
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFTUnregisterLocal, MFTUnregisterLocal function [Media Foundation], mf.mftunregisterlocal, mfapi/MFTUnregisterLocal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFTUnregisterLocal
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFTUnregisterLocal function


## -description


Unregisters one or more Media Foundation transforms (MFTs) from the caller's process.


## -parameters




### -param pClassFactory [in]

A pointer to the <b>IClassFactory</b> interface of a class factory object. This parameter can be <b>NULL</b>.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(<b>ERROR_NOT_FOUND</b>)</b></dt>
</dl>
</td>
<td width="60%">
The MFT specified by the <i>pClassFactory</i> parameter was not registered in this process.

</td>
</tr>
</table>
 




## -remarks



Use this function to unregister a local MFT that was previously registered through the <a href="https://msdn.microsoft.com/802f7083-e224-4e5c-8a35-3e93da0cbd91">MFTRegisterLocal</a> function.

If the <i>pClassFactory</i> parameter is <b>NULL</b>, all local MFTs in the process are unregistered. Otherwise, the function unregisters the MFT associated with the class factory specified by the <i>pClassFactory</i> parameter. In that case, the <i>pClassFactory</i> parameter should equal a pointer value that was previously passed to  the <a href="https://msdn.microsoft.com/802f7083-e224-4e5c-8a35-3e93da0cbd91">MFTRegisterLocal</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

