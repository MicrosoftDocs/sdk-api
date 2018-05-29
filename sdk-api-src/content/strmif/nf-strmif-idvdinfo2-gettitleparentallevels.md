---
UID: NF:strmif.IDvdInfo2.GetTitleParentalLevels
title: IDvdInfo2::GetTitleParentalLevels
author: windows-sdk-content
description: The GetTitleParentalLevels method retrieves the parental levels that are defined for a particular title.
old-location: dshow\idvdinfo2_gettitleparentallevels.htm
old-project: DirectShow
ms.assetid: 00c9d1e5-1b1f-41b3-b06c-0b78e2d2db0b
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetTitleParentalLevels, GetTitleParentalLevels method [DirectShow], GetTitleParentalLevels method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetTitleParentalLevels method, IDvdInfo2.GetTitleParentalLevels, IDvdInfo2::GetTitleParentalLevels, IDvdInfo2GetTitleParentalLevels, dshow.idvdinfo2_gettitleparentallevels, strmif/IDvdInfo2::GetTitleParentalLevels
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdInfo2.GetTitleParentalLevels
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetTitleParentalLevels


## -description



The <code>GetTitleParentalLevels</code> method retrieves the parental levels that are defined for a particular title.




## -parameters




### -param ulTitle [in]

Title for which parental levels are requested. Specify 0xfffffff to return the parental levels for the current title.


### -param pulParentalLevels [out]

Pointer to a variable of type ULONG that receives a bitwise OR combination of <a href="https://msdn.microsoft.com/0b18b5e8-f859-427e-b25f-2f4452492eb9">DVD_PARENTAL_LEVEL</a> values defined for the title.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not initialized.

</td>
</tr>
</table>
 




## -remarks



A title can contain different parental levels for different sections.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/ad996a03-e94e-4743-90a2-aa390984a231">Enforcing Parental Management Levels</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

