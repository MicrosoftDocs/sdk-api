---
UID: NF:certview.IEnumCERTVIEWCOLUMN.Reset
title: IEnumCERTVIEWCOLUMN::Reset
author: windows-sdk-content
description: Moves to the beginning of the column-enumeration sequence.
old-location: security\ienumcertviewcolumn_reset.htm
tech.root: SecCrypto
ms.assetid: 0be00eb0-1a22-4849-95ca-276099bbfa74
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IEnumCERTVIEWCOLUMN interface [Security],Reset method, IEnumCERTVIEWCOLUMN object [Security],Reset method, IEnumCERTVIEWCOLUMN.Reset, IEnumCERTVIEWCOLUMN::Reset, Reset, Reset method [Security], Reset method [Security],IEnumCERTVIEWCOLUMN interface, Reset method [Security],IEnumCERTVIEWCOLUMN object, _certsrv_ienumcertviewcolumn_reset, certview/IEnumCERTVIEWCOLUMN::Reset, security.ienumcertviewcolumn_reset
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
 - IEnumCERTVIEWCOLUMN.Reset
 - IEnumCERTVIEWCOLUMN.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWCOLUMN::Reset


## -description


The <b>Reset</b> method moves to the beginning of the column-enumeration sequence.


## -parameters






## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



Upon successful completion of this method, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa386197(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::Next</a> method to reference the first column in the enumeration. After this second call is made, the information in the column can be obtained by calling one of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386186(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetName</a>: Retrieves the nonlocalized name of the column.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386182(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetDisplayName</a>: Retrieves the localized name of the column.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386192(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetValue</a>: Retrieves the data in the column.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386189(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetType</a>: Retrieves the type of data in the column.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386184(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetMaxLength</a>: Retrieves the maximum length, in bytes, of the column.</li>
</ul>

#### Examples


```cpp
// pEnumCol is previously instantiated IEnumCERTVIEWCOLUMN object
HRESULT    hr;
LONG        Index;
hr = pEnumCol->Reset();
if (S_OK != hr)
    printf("Unable to reset pEnumCol\n");
    // call appropriate error handler / exit routine
else
{
    // now at the beginning of the columns
    // enumerate each column
    while (S_OK == pEnumCol->Next(&Index))
    {
        // Use each column as needed.
    }
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386176(v=VS.85).aspx">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386182(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetDisplayName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386184(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetMaxLength</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386186(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386189(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetType</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386192(v=VS.85).aspx">IEnumCERTVIEWCOLUMN::GetValue</a>
 

 

