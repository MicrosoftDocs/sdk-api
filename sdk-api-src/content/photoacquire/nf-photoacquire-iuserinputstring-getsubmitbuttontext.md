---
UID: NF:photoacquire.IUserInputString.GetSubmitButtonText
title: IUserInputString::GetSubmitButtonText
author: windows-sdk-content
description: The GetSubmitButtonText method retrieves the text for the submit button.
old-location: picacq\iuserinputstring_getsubmitbuttontext.htm
tech.root: acquisition
ms.assetid: 00cb081a-9077-4ecc-9a1f-002072e6ddda
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSubmitButtonText, GetSubmitButtonText method [Picture Acquisition], GetSubmitButtonText method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetSubmitButtonText method, IUserInputString.GetSubmitButtonText, IUserInputString::GetSubmitButtonText, IUserInputStringGetSubmitButtonText, photoacquire/IUserInputString::GetSubmitButtonText, picacq.iuserinputstring_getsubmitbuttontext
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
 - IUserInputString.GetSubmitButtonText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUserInputString::GetSubmitButtonText


## -description



The <code>GetSubmitButtonText</code> method retrieves the text for the submit button.




## -parameters




### -param pbstrSubmitButtonText [out]

Pointer to a string containing the submit button text.


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
 

 

