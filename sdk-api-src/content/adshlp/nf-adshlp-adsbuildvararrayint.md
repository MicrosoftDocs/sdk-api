---
UID: NF:adshlp.ADsBuildVarArrayInt
title: ADsBuildVarArrayInt function (adshlp.h)
author: windows-sdk-content
description: The ADsBuildVarArrayInt function builds a variant array of integers from an array of DWORD values.
old-location: adsi\adsbuildvararrayint.htm
tech.root: adsi
ms.assetid: 61b8a3c1-b8ea-4909-b2a6-f1ce342f396d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ADsBuildVarArrayInt, ADsBuildVarArrayInt function [ADSI], _ds_adsbuildvararrayint, adshlp/ADsBuildVarArrayInt, adsi.adsbuildvararrayint
ms.topic: function
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ADsBuildVarArrayInt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ADsBuildVarArrayInt function


## -description


The <b>ADsBuildVarArrayInt</b> function builds a variant array of integers from an array of <b>DWORD</b> values.


## -parameters




### -param lpdwObjectTypes [in]

Type: <b>LPDWORD</b>

Array of <b>DWORD</b> values.


### -param dwObjectTypes [in]

Type: <b>DWORD</b>

Number of <b>DWORD</b> entries in the given array.


### -param pVar [out]

Type: <b>VARIANT*</b>

Pointer to the resulting variant array of integers.


## -returns



Type: <b>HRESULT</b>

This method supports standard return values.

For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



Use the <b>ADsBuildVarArrayInt</b> function to convert the integer array into a variant array of the integers. The following code example shows how to do this.


```cpp
DWORD dwArray[]={0,1,2,3,4};
long nLength = sizeof(dwArray)/sizeof(DWORD);
VARIANT varArray[nLength];
HRESULT hr = ADsBuildVarArrayInt(dwArray, nLength, varArray);
if (hr = E_FAIL) exit(1);
 
// Resume work with the data in varArray.
. . .
```





## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/7258a840-691a-4d9b-ab33-bcdf30fd1331">ADsBuildVarArrayStr</a>
 

 

