---
UID: NF:certview.IEnumCERTVIEWEXTENSION.GetName
title: IEnumCERTVIEWEXTENSION::GetName (certview.h)
author: windows-sdk-content
description: Retrieves the name of the current extension in the extension-enumeration sequence.
old-location: security\ienumcertviewextension_getname.htm
tech.root: SecCrypto
ms.assetid: 7c56708c-ae25-46f5-94f3-d58eea8d08d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CEnumCERTVIEWEXTENSION object [Security],GetName method, GetName, GetName method [Security], GetName method [Security],CEnumCERTVIEWEXTENSION object, GetName method [Security],IEnumCERTVIEWEXTENSION interface, IEnumCERTVIEWEXTENSION interface [Security],GetName method, IEnumCERTVIEWEXTENSION.GetName, IEnumCERTVIEWEXTENSION::GetName, _certsrv_ienumcertviewextension_getname, certview/IEnumCERTVIEWEXTENSION::GetName, security.ienumcertviewextension_getname
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
 - IEnumCERTVIEWEXTENSION.GetName
 - CEnumCERTVIEWEXTENSION.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWEXTENSION::GetName


## -description


The <b>GetName</b> method retrieves the name of the current extension in the extension-enumeration sequence.

 The returned extension name is an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) string, as in L"2.5.29.31".


## -parameters




### -param pstrOut [out]

A pointer to a value of <b>BSTR</b> type that contains the name of the extension.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and tat the <i>pstrOut</i> parameter is set to the name of the extension.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrOut</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that contains the name of the extension.




## -remarks



This function is used to retrieve the name of the extension currently referenced by the 
extension-enumeration sequence.

If the extension-enumeration sequence is not referencing a valid extension, <b>GetName</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="https://msdn.microsoft.com/7af29b1f-5b43-4ab7-81fa-d03e065f014f">IEnumCERTVIEWEXTENSION::Reset</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/658daf9d-0f61-4c93-9688-a7c74464ca89">IEnumCERTVIEWEXTENSION::Next</a>: Moves to the next extension in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/b354cf0e-2f15-42a5-8e84-4db9bc4e6a8d">IEnumCERTVIEWEXTENSION::Skip</a>: Skips a specified number of extensions.</li>
</ul>

#### Examples


```cpp
BSTR  bstrExtName = NULL;

// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
hr = pEnumExt->GetName(&bstrExtName);
if (S_OK == hr)
    printf("Extension name is: %ws\n", bstrExtName);
else
    printf("GetName failed: %x\n", hr);

// free memory when done
if (NULL != bstrExtName)
    SysFreeString(bstrExtName);
```





## -see-also




<a href="https://msdn.microsoft.com/d5acff51-06f8-4a6f-aa9e-97ba052b1b34">IEnumCERTVIEWEXTENSION</a>



<a href="https://msdn.microsoft.com/c175eba9-ea7c-4018-876a-2db732cb57c4">IEnumCERTVIEWEXTENSION::GetFlags</a>



<a href="https://msdn.microsoft.com/7a81b096-36ba-416a-ad15-5bf1c4d512dd">IEnumCERTVIEWEXTENSION::GetValue</a>



<a href="https://msdn.microsoft.com/658daf9d-0f61-4c93-9688-a7c74464ca89">IEnumCERTVIEWEXTENSION::Next</a>



<a href="https://msdn.microsoft.com/7af29b1f-5b43-4ab7-81fa-d03e065f014f">IEnumCERTVIEWEXTENSION::Reset</a>



<a href="https://msdn.microsoft.com/b354cf0e-2f15-42a5-8e84-4db9bc4e6a8d">IEnumCERTVIEWEXTENSION::Skip</a>
 

 

