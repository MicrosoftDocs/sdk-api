---
UID: NN:faxcomex.IFaxDocument2
title: IFaxDocument2 (faxcomex.h)
author: windows-sdk-content
description: Defines a messaging object used by a fax client application to compose a fax document and submit it to the fax service for processing.
old-location: fax\_mfax_faxdocument2_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxdocument2\faxinta_n_faxdocument2_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxDocument2, IFaxDocument2 interface [Fax Service], IFaxDocument2 interface [Fax Service],described, _mfax_faxdocument2_cpp, fax._mfax_faxdocument2_cpp, faxcomex/IFaxDocument2
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxDocument2"
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxDocument2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxDocument2 interface


## -description


Defines a messaging object used by a fax client application to compose a fax document and submit it to the fax service for processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDocument2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>. <b>IFaxDocument2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxDocument2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdocument2-connectedsubmit2-vb">ConnectedSubmit2</a>
</td>
<td align="left" width="63%">
Submits one or more fax documents to the connected <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>. This method returns an array of fax job ID strings, one for each recipient of the fax.



<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdocument2-submit2-vb">Submit2</a>
</td>
<td align="left" width="63%">
Submits one or more documents to the fax service for processing.



<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDocument2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdocument2-bodies-vb">Bodies</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Provides a collection of one or more documents to the fax document. 



<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdocument2-submissionid-vb">SubmissionId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the submission identifier for the fax document. Every job in a given broadcast receives the same submission identifier.



<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
</table> 


## -remarks



A default implementation of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a> and <b>IFaxDocument2</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>
 

 

