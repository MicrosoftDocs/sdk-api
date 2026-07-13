---
UID: NF:xpsobjectmodel.IXpsOMPageReference.CollectLinkTargets
title: IXpsOMPageReference::CollectLinkTargets (xpsobjectmodel.h)
description: Gets an IXpsOMNameCollection interface that contains the names of all the document subtree objects whose IsHyperlinkTarget property is set to TRUE.
helpviewer_keywords: ["CollectLinkTargets","CollectLinkTargets method [XPS Documents and Packaging]","CollectLinkTargets method [XPS Documents and Packaging]","IXpsOMPageReference interface","IXpsOMPageReference interface [XPS Documents and Packaging]","CollectLinkTargets method","IXpsOMPageReference.CollectLinkTargets","IXpsOMPageReference::CollectLinkTargets","xps.ixpsompagereference_collectlinktargets","xpsobjectmodel/IXpsOMPageReference::CollectLinkTargets"]
old-location: xps\ixpsompagereference_collectlinktargets.htm
tech.root: xps
ms.assetid: 82c64e8a-d8fb-41e3-95f8-b8ca490eae78
ms.date: 12/05/2018
ms.keywords: CollectLinkTargets, CollectLinkTargets method [XPS Documents and Packaging], CollectLinkTargets method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],CollectLinkTargets method, IXpsOMPageReference.CollectLinkTargets, IXpsOMPageReference::CollectLinkTargets, xps.ixpsompagereference_collectlinktargets, xpsobjectmodel/IXpsOMPageReference::CollectLinkTargets
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMPageReference::CollectLinkTargets
 - xpsobjectmodel/IXpsOMPageReference::CollectLinkTargets
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPageReference.CollectLinkTargets
---

# IXpsOMPageReference::CollectLinkTargets


## -description

Gets an  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection">IXpsOMNameCollection</a> interface that contains the names of all the document subtree objects whose  <b>IsHyperlinkTarget</b> property is set to <b>TRUE</b>.

## -parameters

### -param linkTargets [out, retval]

A pointer to an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection">IXpsOMNameCollection</a> interface that contains the names of all the document subtree objects whose <b>IsHyperlinkTarget</b> property is set to <b>TRUE</b>. If no such objects exist in the document, the <b>IXpsOMNameCollection</b> interface will be empty.

<div class="alert"><b>Note</b>  Every time this method is called, it returns a new collection.</div>
<div> </div>

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>linkTargets</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

If the page is originally loaded from a package but  is not currently loaded in the object model, this method returns the values specified in the original <b>PageContent.LinkTargets</b> markup.
      

If the document does not have any link targets, the name collection returned in <i>linkTargets</i> will be empty.

To get the number of elements in the collection that is returned in <i>linkTargets</i>, call the collection's <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomnamecollection-getcount">GetCount</a> method.

This method returns the pointer to a new collection every time it is called. To prevent a memory leak, the pointer to a previous collection should be released when it is no longer needed or before the pointer variable is reused for another call to this method. The following code example shows how this can be done in a program.


```cpp
    HRESULT                         hr = S_OK;
    IXpsOMPage                      *page = NULL;
    IXpsOMNameCollection            *linkTargets = NULL;

    UINT32 numTargets = 0;
    UINT32 thisTarget = 0;
    LPWSTR thisTargetName = NULL;

    // pageRef contains the current page reference 

    // if the page hasn't been loaded yet, for example, if the XPS OM 
    //  was loaded from an XPS document, CollectLinkTargets obtains the
    //  list of link targets from the <PageContent.LinkTargets> markup
    hr = pageRef->CollectLinkTargets(&linkTargets);

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);

    // after the page object has been loaded and calling GetPage or 
    //  by creating a page in the XPS OM, CollectLinkTargets will now check
    //  each of the page elements to return the list so this call to
    //  CollectLinkTargets might take longer to return than the previous
    //  call above if the XPS OM was created from a file
    linkTargets->Release(); // release previous collection
    hr = pageRef->CollectLinkTargets(&linkTargets);
    
    // walk the list of link targets returned
    hr = linkTargets->GetCount( &numTargets );
    thisTarget = 0;
    while (thisTarget < numTargets) {
        hr = linkTargets->GetAt (thisTarget, &thisTargetName);
        printf ("%s\n", thisTargetName);
        // release the target string returned to prevent memory leaks
        CoTaskMemFree (thisTargetName);
        // get next target in list
        thisTarget++;
    }
    // release page and the link target collection
    page->Release();
    linkTargets->Release();

```

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection">IXpsOMNameCollection</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>