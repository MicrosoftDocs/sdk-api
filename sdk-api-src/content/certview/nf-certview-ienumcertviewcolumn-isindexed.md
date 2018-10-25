---
UID: NF:certview.IEnumCERTVIEWCOLUMN.IsIndexed
title: IEnumCERTVIEWCOLUMN::IsIndexed
author: windows-sdk-content
description: Reports whether the data in the column is indexed.
old-location: security\ienumcertviewcolumn_isindexed.htm
tech.root: seccrypto
ms.assetid: 7373c0c3-3a1d-4a32-90e6-0f0575a0b61b
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IEnumCERTVIEWCOLUMN interface [Security],IsIndexed method, IEnumCERTVIEWCOLUMN.IsIndexed, IEnumCERTVIEWCOLUMN::IsIndexed, IsIndexed, IsIndexed method [Security], IsIndexed method [Security],IEnumCERTVIEWCOLUMN interface, _certsrv_ienumcertviewcolumn_isindexed, certview/IEnumCERTVIEWCOLUMN::IsIndexed, security.ienumcertviewcolumn_isindexed
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certview.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IEnumCERTVIEWCOLUMN.IsIndexed
 - IEnumCERTVIEWCOLUMN.IsIndexed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWCOLUMN::IsIndexed


## -description


The <b>IsIndexed</b> method reports whether the data in the column is indexed.


## -parameters




### -param pIndexed [out]

A pointer to a variable of type <b>LONG</b> that indicates <b>TRUE</b> if the data is indexed and <b>FALSE</b> if the data is not indexed. This method fails if <i>pIndexed</i> is set to <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the <i>pIndexed</i> is set to <b>TRUE</b> or <b>FALSE</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 One if the column is indexed; otherwise, zero.




## -remarks



This method is used to determine whether the data of the current column referenced by the column-enumeration sequence is indexed.

If the column-enumeration sequence is not referencing a valid column, <b>IsIndexed</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386199(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386197(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Next</a>: Moves to the next column in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386201(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Skip</a>: Skips a specified number of columns.</li>
</ul>

#### Examples


```cpp
HRESULT  hr;
LONG     bIsindexed;

// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
hr = pEnumCol->IsIndexed(&bIsindexed);
if (S_OK == hr)
    printf( bIsindexed ? "Indexed\n" : "Not indexed\n");
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386176(v=VS.85).aspx">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386197(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Next</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386199(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Reset</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386201(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Skip</a>
 

 

