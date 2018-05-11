---
UID: NF:propsys.PSCreatePropertyChangeArray
title: PSCreatePropertyChangeArray function
author: windows-driver-content
description: Creates a container for a set of IPropertyChange objects. This container can be used with IFileOperation to apply a set of property changes to a set of files.
old-location: properties\PSCreatePropertyChangeArray.htm
old-project: properties
ms.assetid: 5e0fdf09-a688-4297-9abe-2f1d67fce1a2
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PSCreatePropertyChangeArray, PSCreatePropertyChangeArray function [Windows Properties], _shell_PSCreatePropertyChangeArray, properties.PSCreatePropertyChangeArray, propsys/PSCreatePropertyChangeArray, shell.PSCreatePropertyChangeArray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PSCreatePropertyChangeArray
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PSCreatePropertyChangeArray function


## -description


Creates a container for a set of <a href="shell.IPropertyChange">IPropertyChange</a> objects. This container can be used with <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> to apply a set of property changes to a set of files.


## -parameters




### -param rgpropkey [in, optional]

Type: <b>const <a href="shell.PROPERTYKEY">PROPERTYKEY</a>*</b>

Pointer to an array of <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structures that name the specific properties whose changes are being stored. If this value is <b>NULL</b>, <i>cChanges</i> must be 0.


### -param rgflags [in, optional]

Type: <b>const <a href="shell.PKA_FLAGS">PKA_FLAGS</a>*</b>

Pointer to an array of <a href="shell.PKA_FLAGS">PKA_FLAGS</a> values. If this value is <b>NULL</b>, <i>cChanges</i> must be 0.


### -param rgpropvar [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures. If this value is <b>NULL</b>, <i>cChanges</i> must be 0.


### -param cChanges [in]

Type: <b>UINT</b>

Count of changes to be applied. This is the number of elements in each of the arrays <i>rgpropkey</i>, <i>rgflags</i>, and <i>rgpropvar</i>.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the ID of the requested interface.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="shell.IPropertyChangeArray">IPropertyChangeArray</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates a Component Object Model (COM) object that implements <a href="shell.IPropertyChangeArray">IPropertyChangeArray</a>. This object is a container for a set of <a href="shell.IPropertyChange">IPropertyChange</a> interfaces and can be used with <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> to apply a set of property changes to a set of files.

You must initialize COM with <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> before you call <a href="shell.PSCreatePropertyChangeArray">PSCreatePropertyChangeArray</a>. COM must remain initialized for the lifetime of this object. The property change array executes in a single-threaded apartment (STA).

A property change array can be initialized either by specifying simple changes by using the parameters, or by using various <a href="shell.IPropertyChangeArray">IPropertyChangeArray</a> methods to insert or append additional changes.

The parameters are tied together by their index value. For instance, for property rgpropkey[0], the new value rgpropvar[0] is applied as specified by rgflags[0]. The <i>cChanges</i> parameter states how many of these sets there are. Therefore, the number of elements in each array should be the same: ARRAYSIZE(rgpropkey) = ARRAYSIZE(rgflags) = ARRAYSIZE(rgpropvar) = cChanges.


<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> applies all changes in the property change array to a file simultaneously to avoid opening the file multiple times.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSCreatePropertyChangeArray">PSCreatePropertyChangeArray</a> to set the <a href="shell.props_System_Comment">Comment</a> property to "Fun" and <a href="shell.props_System_Rating">Rating</a> to 4 on one or more files.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IFileOperation *pfo;
// Assume variable pfo has been initialized by calling SetOperationFlags, 
// ApplyPropertiesToItems, and SetProgressMessage as appropriate.
 
PROPVARIANT rgpropvar[2] = {0};

HRESULT hr = InitPropVariantFromString(L"Fun", &amp;rgpropvar[0]);

if (SUCCEEDED(hr))
{
    hr = InitPropVariantFromUInt32(RATING_FOUR_STARS_SET, &amp;rgpropvar[1]);

    if (SUCCEEDED(hr))
    {
        REFPROPERTYKEY rgkey[2] = {PKEY_Comment, PKEY_Rating};
        PKA_FLAGS rgflags[2] = {PKA_SET, PKA_SET};
        IPropertyChangeArray *pChangeArray;

        hr = PSCreatePropertyChangeArray(rgkey, rgflags, rgpropvar, 2, IID_PPV_ARGS(&amp;pChangeArray));

        if (SUCCEEDED(hr))
        {
            hr = pfo-&gt;SetProperties(pChangeArray);

            if (SUCCEEDED(hr))
            {
                hr = pfo-&gt;PerformOperations();
            }
            pChangeArray-&gt;Release();
        }
    }
    ClearPropVariantArray(rgpropvar, ARRAYSIZE(rgpropvar));
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PSCreateSimplePropertyChange">PSCreateSimplePropertyChange</a>
 

 

