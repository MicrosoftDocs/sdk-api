---
UID: NF:propvarutil.InitVariantFromGUIDAsString
title: InitVariantFromGUIDAsString function
author: windows-sdk-content
description: Initializes a VARIANT structure based on a GUID. The structure is initialized as a VT_BSTR type.
old-location: properties\InitVariantFromGUIDAsString.htm
old-project: properties
ms.assetid: 2a78257a-a8ce-45e8-aea2-dfa9f380528a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitVariantFromGUIDAsString, InitVariantFromGUIDAsString function [Windows Shell], _shell_InitVariantFromGUIDAsString, properties.InitVariantFromGUIDAsString, propvarutil/InitVariantFromGUIDAsString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - InitVariantFromGUIDAsString
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# InitVariantFromGUIDAsString function


## -description


Initializes a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure based on a <b>GUID</b>. The structure is initialized as a <b>VT_BSTR</b> type.


## -parameters




### -param guid [in]

Type: <b>REFGUID</b>

Reference to the source <b>GUID</b>.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_BSTR variant, formatting the GUID in a form similar to <code>{c200e360-38c5-11ce-ae62-08002b2b79ef}</code>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <b>InitVariantFromGUIDAsString</b>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromGUIDAsString(FMTID_DocSummaryInformation, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_BSTR.
    VariantClear(&var);
}
```





## -see-also




<a href="https://msdn.microsoft.com/a48a8927-2718-4f9c-96f2-ab370206550b">InitPropVariantFromCLSID</a>



<a href="https://msdn.microsoft.com/c46c1263-527a-4a64-b4c9-4c4779b271c7">InitVariantFromGUIDAsBuffer</a>



<a href="https://msdn.microsoft.com/1af84b55-da7e-430c-97fe-1c544a40c039">VariantToGUID</a>



<a href="https://msdn.microsoft.com/4850f9b8-8f86-4428-bf3b-f3abdc6047c1">VariantToString</a>
 

 

