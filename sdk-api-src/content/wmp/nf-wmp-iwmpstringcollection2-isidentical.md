---
UID: NF:wmp.IWMPStringCollection2.isIdentical
title: IWMPStringCollection2::isIdentical
author: windows-sdk-content
description: The isIdentical method retrieves a value indicating whether the supplied object is the same as the current one.
old-location: wmp\iwmpstringcollection2_isidentical.htm
old-project: WMP
ms.assetid: 549fdee8-7cd4-4ceb-8ed1-0de467d6c348
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPStringCollection2 interface [Windows Media Player],isIdentical method, IWMPStringCollection2.isIdentical, IWMPStringCollection2::isIdentical, IWMPStringCollection2isIdentical, isIdentical, isIdentical method [Windows Media Player], isIdentical method [Windows Media Player],IWMPStringCollection2 interface, wmp.iwmpstringcollection2_isidentical, wmp/IWMPStringCollection2::isIdentical
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPStringCollection2.isIdentical
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPStringCollection2::isIdentical


## -description



The <b>isIdentical</b> method retrieves a value indicating whether the supplied object is the same as the current one.




## -parameters




### -param pIWMPStringCollection2 [in]

Pointer to an <b>IWMPStringCollection2</b> interface that represents the object to compare with current one.


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



To use this method, read access to the library is required. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/7aeaf549-3c60-4dd8-9e46-6bab357f4960">IWMPStringCollection2 Interface</a>
 

 

