---
UID: NF:wmp.IWMPLibrary.isIdentical
title: IWMPLibrary::isIdentical (wmp.h)
description: The isIdentical method retrieves a value that indicates whether the supplied object is the same as the current one.
helpviewer_keywords: ["IWMPLibrary interface [Windows Media Player]","isIdentical method","IWMPLibrary.isIdentical","IWMPLibrary::isIdentical","IWMPLibraryisIdentical","isIdentical","isIdentical method [Windows Media Player]","isIdentical method [Windows Media Player]","IWMPLibrary interface","wmp.iwmplibrary_isidentical","wmp/IWMPLibrary::isIdentical"]
old-location: wmp\iwmplibrary_isidentical.htm
tech.root: WMP
ms.assetid: af121fc7-6a9a-4c1a-bea4-433e62ca19e3
ms.date: 12/05/2018
ms.keywords: IWMPLibrary interface [Windows Media Player],isIdentical method, IWMPLibrary.isIdentical, IWMPLibrary::isIdentical, IWMPLibraryisIdentical, isIdentical, isIdentical method [Windows Media Player], isIdentical method [Windows Media Player],IWMPLibrary interface, wmp.iwmplibrary_isidentical, wmp/IWMPLibrary::isIdentical
f1_keywords:
- wmp/IWMPLibrary.isIdentical
dev_langs:
- c++
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPLibrary.isIdentical
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPLibrary::isIdentical


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmplibrary">IWMPLibrary Interface</a>
 

 

