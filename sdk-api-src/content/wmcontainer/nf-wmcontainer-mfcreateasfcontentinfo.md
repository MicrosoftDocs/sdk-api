---
UID: NF:wmcontainer.MFCreateASFContentInfo
title: MFCreateASFContentInfo function
author: windows-sdk-content
description: Creates the ASF Header Object object.
old-location: mf\mfcreateasfcontentinfo.htm
tech.root: medfound
ms.assetid: 00460f79-7033-4893-88c0-b1c939441f70
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 00460f79-7033-4893-88c0-b1c939441f70, MFCreateASFContentInfo, MFCreateASFContentInfo function [Media Foundation], mf.mfcreateasfcontentinfo, wmcontainer/MFCreateASFContentInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFContentInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateASFContentInfo function


## -description



Creates the <a href="https://msdn.microsoft.com/en-us/library/Ee663575(v=VS.85).aspx">ASF Header Object</a> object.




## -parameters




### -param ppIContentInfo

Receives a pointer to the <a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a> interface. The caller must release the interface.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

