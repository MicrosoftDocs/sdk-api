---
UID: NF:wmp.IWMPLibrary.isIdentical
title: IWMPLibrary::isIdentical method
author: windows-driver-content
description: The isIdentical method retrieves a value that indicates whether the supplied object is the same as the current one.
old-location: wmp\iwmplibrary_isidentical.htm
old-project: WMP
ms.assetid: af121fc7-6a9a-4c1a-bea4-433e62ca19e3
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPLibrary, IWMPLibrary interface [Windows Media Player], isIdentical method, IWMPLibrary::isIdentical, IWMPLibraryisIdentical, isIdentical method [Windows Media Player], isIdentical method [Windows Media Player], IWMPLibrary interface, isIdentical,IWMPLibrary.isIdentical, wmp.iwmplibrary_isidentical, wmp/IWMPLibrary::isIdentical
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPLibrary.isIdentical
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPLibrary::isIdentical method


## -description



The <b>isIdentical</b> method retrieves a value that indicates whether the supplied object is the same as the current one.




## -parameters




### -param pIWMPLibrary [in]

Pointer to an <b>IWMPLibrary</b> interface that represents the object to compare with current one.


### -param pvbool [out]

Pointer to a <b>VARIANT_BOOL</b> that receives the result of the comparison. VARIANT_TRUE indicates that the objects are the same.


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



<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/add0ed43-d83f-4793-b1f6-ccad0f01854c">IWMPLibrary Interface</a>
 

 

