---
UID: NF:wmcontainer.MFCreateASFProfile
title: MFCreateASFProfile function
author: windows-sdk-content
description: Creates the ASF profile object.
old-location: mf\mfcreateasfprofile.htm
old-project: medfound
ms.assetid: fa57fac7-a191-4d5b-89be-319af7b3e09c
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MFCreateASFProfile, MFCreateASFProfile function [Media Foundation], fa57fac7-a191-4d5b-89be-319af7b3e09c, mf.mfcreateasfprofile, wmcontainer/MFCreateASFProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFProfile
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# MFCreateASFProfile function


## -description



Creates the ASF profile object.




## -parameters




### -param ppIProfile

Receives a pointer to the <a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a> interface. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

