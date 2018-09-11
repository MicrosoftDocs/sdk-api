---
UID: NN:xpsobjectmodel.IXpsOMDocumentSequence
title: IXpsOMDocumentSequence
author: windows-sdk-content
description: The root object that has the XPS document content.
old-location: xps\ixpsomdocumentsequence.htm
tech.root: printdocs
ms.assetid: 472095a4-ecd8-406a-97c2-1a34b4e5184a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMDocumentSequence, IXpsOMDocumentSequence interface [XPS Documents and Packaging], IXpsOMDocumentSequence interface [XPS Documents and Packaging],described, xps.ixpsomdocumentsequence, xpsobjectmodel/IXpsOMDocumentSequence
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMDocumentSequence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMDocumentSequence interface


## -description


The root object that has the XPS document content.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMDocumentSequence</b> interface inherits from <a href="https://msdn.microsoft.com/71cd0155-6c95-42ca-bfc3-dffd43d95dc9">IXpsOMPart</a>. <b>IXpsOMDocumentSequence</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMDocumentSequence</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d924e610-1142-4623-b64b-219558fb07d6">GetDocuments</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/4f3acae9-10a0-47ff-9170-a40abe230580">IXpsOMDocumentCollection</a> interface, which contains the documents specified in the document sequence.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5c59e70-d7b5-42cf-a979-6da4899203ba">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a> interface that contains the document sequence.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d53d537-8db1-4e39-98e6-8987dbf5fc27">GetPrintTicketResource</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface to the job-level print ticket that is  assigned to the document sequence.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfc5889d-ab1d-4dbe-af11-625ee5e8c95f">SetPrintTicketResource</a>
</td>
<td align="left" width="63%">
Sets the job-level print ticket resource for the document sequence.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMDocumentSequence    *newInterface;
IOpcPartUri               *partUri;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast<LPVOID*>(&xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory->CreatePartUri(partUriString, &partUri);
    
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory->CreateDocumentSequence (partUri, &newInterface);

        if (SUCCEEDED(hr))
        {
            // use newInterface

            newInterface->Release();
        }
        partUri->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```





## -see-also




<a href="https://msdn.microsoft.com/51d42b34-3380-4464-8feb-d03935f88077">IXpsOMObjectFactory::CreateDocumentSequence</a>



<a href="https://msdn.microsoft.com/71cd0155-6c95-42ca-bfc3-dffd43d95dc9">IXpsOMPart</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

