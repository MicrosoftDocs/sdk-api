---
UID: NF:photoacquire.IUserInputString.GetStringId
title: IUserInputString::GetStringId
author: windows-sdk-content
description: The GetStringId method retrieves the unlocalized canonical name for the requested string. For example, when requesting a tag name, the canonical name might be &#0034;TagName&#0034;.
old-location: picacq\iuserinputstring_getstringid.htm
tech.root: acquisition
ms.assetid: 29c4b592-fa6a-4f9b-a390-e8bc0928a26d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetStringId, GetStringId method [Picture Acquisition], GetStringId method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetStringId method, IUserInputString.GetStringId, IUserInputString::GetStringId, IUserInputStringGetStringId, photoacquire/IUserInputString::GetStringId, picacq.iuserinputstring_getstringid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IUserInputString.GetStringId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUserInputString::GetStringId


## -description



The <b>GetStringId</b> method retrieves the unlocalized canonical name for the requested string. For example, when requesting a tag name, the canonical name might be "TagName".




## -parameters




### -param pbstrStringId [out]

Pointer to a string containing the string identifier (ID).


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was passed where a non-<b>NULL</b> pointer is expected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f942fefc-2db1-4067-8311-f9ebbaca9d31">IUserInputString Interface</a>
 

 

