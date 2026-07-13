---
UID: NF:roparameterizediid.RoGetParameterizedTypeInstanceIID
title: RoGetParameterizedTypeInstanceIID function (roparameterizediid.h)
description: Computes the interface identifier (IID) of the interface or delegate type that results when a parameterized interface or delegate is instantiated with the specified type arguments.
helpviewer_keywords: ["RoGetParameterizedTypeInstanceIID","RoGetParameterizedTypeInstanceIID function [Windows Runtime]","roparameterizediid/RoGetParameterizedTypeInstanceIID","winrt.rogetparameterizedtypeinstanceiid"]
old-location: winrt\rogetparameterizedtypeinstanceiid.htm
tech.root: WinRT
ms.assetid: DE908C82-5D7C-415C-B08B-31786589979B
ms.date: 12/05/2018
ms.keywords: RoGetParameterizedTypeInstanceIID, RoGetParameterizedTypeInstanceIID function [Windows Runtime], roparameterizediid/RoGetParameterizedTypeInstanceIID, winrt.rogetparameterizedtypeinstanceiid
req.header: roparameterizediid.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OneCore.Lib
req.dll: Api-ms-win-core-winrt-roparameterizediid-l1-1-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoGetParameterizedTypeInstanceIID
 - roparameterizediid/RoGetParameterizedTypeInstanceIID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-winrt-roparameterizediid-l1-1-0.dll
 - ComBase.dll
api_name:
 - RoGetParameterizedTypeInstanceIID
---

# RoGetParameterizedTypeInstanceIID function


## -description

Computes the interface identifier (IID) of the interface or delegate type that results when a parameterized interface or delegate is instantiated with the specified type arguments.

## -parameters

### -param nameElementCount

Type: <b>UINT32</b>

Number of elements in <i>nameElements.</i>

### -param nameElements [in]

Type: <b>PCWSTR*</b>

A parsed Windows Runtime type name, as returned by the <a href="/windows/desktop/api/rometadataresolution/nf-rometadataresolution-roparsetypename">RoParseTypeName</a> function.
For example, "Windows.Foundation.Collections.IVector`1", and "N1.N2.IFoo".

### -param metaDataLocator [in]

Type: <b>const <a href="/windows/desktop/api/roparameterizediid/ns-roparameterizediid-irometadatalocator">IRoMetaDataLocator</a></b>

A callback to use for resolving metadata. 
                                                                  
An implementation should use the <a href="/windows/desktop/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile">RoGetMetaDataFile</a> function to discover the necessary metadata (.winmd) file and examine the metadata to determine the necessary type information. Because the <b>RoGetMetaDataFile</b> function does not cache results, locators should cache the results as appropriate for the programming model being implemented.

### -param iid [out]

Type: <b>GUID*</b>

The IID of the interface or delegate that corresponds with <i>nameElements</i>.

### -param pExtra [out, optional]

Type: <b>ROPARAMIIDHANDLE*</b>

Handle to the IID that corresponds with <i>nameElements</i>.

## -returns

Type: <b>HRESULT</b>

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
The call was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available to complete the task.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The wrong number of type arguments are provided for a parameterized type.

</td>
</tr>
</table>
 

A failure may also occur if a type is inappropriate for the context in which it appears.

## -remarks

The <b>RoGetParameterizedTypeInstanceIID</b> function is for use by programming language implementers.

This function is stateless.  The <i>metaDataLocator</i> argument is not preserved between calls and may be released as soon as the call returns.



The <b>RoGetParameterizedTypeInstanceIID</b> function does not perform deep semantic analysis.  For instance, if <a href="/windows/desktop/api/roparameterizediid/ns-roparameterizediid-irosimplemetadatabuilder">IRoSimpleMetaDataBuilder</a> specifies that a structure contains an interface pointer, this function returns success, even though such metadata is semantically invalid. The value of the returned IID is unspecified in such cases.

This function may recursively invoke the metadata locator provided as an argument.



If a call to the <a href="/windows/desktop/api/roparameterizediid/ns-roparameterizediid-irosimplemetadatabuilder">IRoSimpleMetaDataBuilder</a> function fails, this function will return that failure code.




#### Examples


```cpp

#include <stdlib.h>
#include <windows.h>
#include <winrt/paraminstanceapi.h>

HRESULT ExampleMetadataLocator(
    PCWSTR name, 
    IRoSimpleMetaDataBuilder& builder)
{
    if (wcscmp(L"Example.IParam`1", name) == 0)
    {
        GUID piidParam= { /* 22046e87-28b5-4c53-9804-bc69f6ee0299 */
            0x22046e87,
            0x28b5,
            0x4c53,
            {0x98, 0x04, 0xbc, 0x69, 0xf6, 0xee, 0x02, 0x99}
        };
        builder.SetParameterizedInterface(piidParam, 1);
    }
    else if (wcscmp(L"Example.InterfaceGroup", name) == 0)
    {
        builder.SetInterfaceGroupSimpleDefault(name, L"Example.IFoo", nullptr);
    }
    else if (wcscmp(L"Example.IFoo", name) == 0)
    {
        GUID iidFoo = { /* f7f968c2-b1d8-47e0-98db-1b04f2bba657 */
            0xf7f968c2,
            0xb1d8,
            0x47e0,
            {0x98, 0xdb, 0x1b, 0x04, 0xf2, 0xbb, 0xa6, 0x57}
        };
        builder.SetWinRtInterface(iidFoo);
    }
    return E_ABORT;
}

int main()
{
    // example, compute IID
    GUID iidResult;
    PCWSTR names = { L"Example.IParam`1", L"Example.InterfaceGroup" };
    HRESULT hr = RoGetParameterizedTypeInstanceIID(
        2,
        names,
        Ro::Locator(&ExampleMetadataLocator),
        &iidResult);
}


```