---
UID: NF:propsys.PSCreatePropertyChangeArray
title: PSCreatePropertyChangeArray function (propsys.h)
description: Creates a container for a set of IPropertyChange objects. This container can be used with IFileOperation to apply a set of property changes to a set of files.
helpviewer_keywords: ["PSCreatePropertyChangeArray","PSCreatePropertyChangeArray function [Windows Properties]","_shell_PSCreatePropertyChangeArray","properties.PSCreatePropertyChangeArray","propsys/PSCreatePropertyChangeArray","shell.PSCreatePropertyChangeArray"]
old-location: properties\PSCreatePropertyChangeArray.htm
tech.root: properties
ms.assetid: 5e0fdf09-a688-4297-9abe-2f1d67fce1a2
ms.date: 12/05/2018
ms.keywords: PSCreatePropertyChangeArray, PSCreatePropertyChangeArray function [Windows Properties], _shell_PSCreatePropertyChangeArray, properties.PSCreatePropertyChangeArray, propsys/PSCreatePropertyChangeArray, shell.PSCreatePropertyChangeArray
req.header: propsys.h
req.include-header: 
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
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSCreatePropertyChangeArray
 - propsys/PSCreatePropertyChangeArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSCreatePropertyChangeArray
---

# PSCreatePropertyChangeArray function


## -description

Creates a container for a set of <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychange">IPropertyChange</a> objects. This container can be used with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> to apply a set of property changes to a set of files.

## -parameters

### -param rgpropkey [in, optional]

Type: <b>const <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures that name the specific properties whose changes are being stored. If this value is <b>NULL</b>, <i>cChanges</i> must be 0.

### -param rgflags [in, optional]

Type: <b>const <a href="/windows/desktop/api/propsys/ne-propsys-pka_flags">PKA_FLAGS</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/propsys/ne-propsys-pka_flags">PKA_FLAGS</a> values. If this value is <b>NULL</b>, <i>cChanges</i> must be 0.

### -param rgpropvar [in, optional]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures. If this value is <b>NULL</b>, <i>cChanges</i> must be 0.

### -param cChanges [in]

Type: <b>UINT</b>

Count of changes to be applied. This is the number of elements in each of the arrays <i>rgpropkey</i>, <i>rgflags</i>, and <i>rgpropvar</i>.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the ID of the requested interface.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychangearray">IPropertyChangeArray</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates a Component Object Model (COM) object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychangearray">IPropertyChangeArray</a>. This object is a container for a set of <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychange">IPropertyChange</a> interfaces and can be used with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> to apply a set of property changes to a set of files.

You must initialize COM with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> before you call <a href="/windows/desktop/api/propsys/nf-propsys-pscreatepropertychangearray">PSCreatePropertyChangeArray</a>. COM must remain initialized for the lifetime of this object. The property change array executes in a single-threaded apartment (STA).

A property change array can be initialized either by specifying simple changes by using the parameters, or by using various <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychangearray">IPropertyChangeArray</a> methods to insert or append additional changes.

The parameters are tied together by their index value. For instance, for property rgpropkey[0], the new value rgpropvar[0] is applied as specified by rgflags[0]. The <i>cChanges</i> parameter states how many of these sets there are. Therefore, the number of elements in each array should be the same: ARRAYSIZE(rgpropkey) = ARRAYSIZE(rgflags) = ARRAYSIZE(rgpropvar) = cChanges.


<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> applies all changes in the property change array to a file simultaneously to avoid opening the file multiple times.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-pscreatepropertychangearray">PSCreatePropertyChangeArray</a> to set the <a href="/windows/desktop/Tapi/comment-ovr">Comment</a> property to "Fun" and <a href="/windows/desktop/wmformat/rating">Rating</a> to 4 on one or more files.


```cpp
// IFileOperation *pfo;
// Assume variable pfo has been initialized by calling SetOperationFlags, 
// ApplyPropertiesToItems, and SetProgressMessage as appropriate.
 
PROPVARIANT rgpropvar[2] = {0};

HRESULT hr = InitPropVariantFromString(L"Fun", &rgpropvar[0]);

if (SUCCEEDED(hr))
{
    hr = InitPropVariantFromUInt32(RATING_FOUR_STARS_SET, &rgpropvar[1]);

    if (SUCCEEDED(hr))
    {
        REFPROPERTYKEY rgkey[2] = {PKEY_Comment, PKEY_Rating};
        PKA_FLAGS rgflags[2] = {PKA_SET, PKA_SET};
        IPropertyChangeArray *pChangeArray;

        hr = PSCreatePropertyChangeArray(rgkey, rgflags, rgpropvar, 2, IID_PPV_ARGS(&pChangeArray));

        if (SUCCEEDED(hr))
        {
            hr = pfo->SetProperties(pChangeArray);

            if (SUCCEEDED(hr))
            {
                hr = pfo->PerformOperations();
            }
            pChangeArray->Release();
        }
    }
    ClearPropVariantArray(rgpropvar, ARRAYSIZE(rgpropvar));
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pscreatesimplepropertychange">PSCreateSimplePropertyChange</a>