---
UID: NF:certview.ICertView.OpenView
title: ICertView::OpenView (certview.h)
description: Opens a view to a Certificate Services database and instantiates an instance of an IEnumCERTVIEWROW object.
helpviewer_keywords: ["CCertView object [Security]","OpenView method","ICertView interface [Security]","OpenView method","ICertView.OpenView","ICertView2 interface [Security]","OpenView method","ICertView2::OpenView","ICertView::OpenView","OpenView","OpenView method [Security]","OpenView method [Security]","CCertView object","OpenView method [Security]","ICertView interface","OpenView method [Security]","ICertView2 interface","certview/ICertView2::OpenView","certview/ICertView::OpenView","security.icertview2_openview"]
old-location: security\icertview2_openview.htm
tech.root: security
ms.assetid: d68a5463-f711-4737-b0ad-889f7e4855d5
ms.date: 12/05/2018
ms.keywords: CCertView object [Security],OpenView method, ICertView interface [Security],OpenView method, ICertView.OpenView, ICertView2 interface [Security],OpenView method, ICertView2::OpenView, ICertView::OpenView, OpenView, OpenView method [Security], OpenView method [Security],CCertView object, OpenView method [Security],ICertView interface, OpenView method [Security],ICertView2 interface, certview/ICertView2::OpenView, certview/ICertView::OpenView, security.icertview2_openview
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertView::OpenView
 - certview/ICertView::OpenView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertView2.OpenView
 - ICertView.OpenView
 - CCertView.OpenView
---

# ICertView::OpenView


## -description

The <b>OpenView</b> method opens a view to a Certificate Services database and instantiates an instance of an <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a> object.

## -parameters

### -param ppenum [out]

A pointer to a pointer of <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a> type.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is an <a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a> object.

## -remarks

Before calling the <b>OpenView</b> method, it is necessary to establish a connection with a Certificate Services server by calling the 
<a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">OpenConnection</a> method first.

The 
<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a> object returned by this call represents a row-enumeration sequence whose internal index is pointing to the beginning of the sequence. To look at the first row in the sequence, call the  
<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">IEnumCERTVIEWROW::Next</a> method, which moves the internal index to the first row.

To view a nondefault column set or a subset of the rows, call 
<a href="/windows/desktop/api/certview/nf-certview-icertview-setresultcolumncount">SetResultColumnCount</a>, 
<a href="/windows/desktop/api/certview/nf-certview-icertview-setresultcolumn">SetResultColumn</a>, and 
<a href="/windows/desktop/api/certview/nf-certview-icertview-setrestriction">SetRestriction</a> after calling <a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">OpenConnection</a> and before calling <b>OpenView</b>.


#### Examples


```cpp
// pCertView is previously instantiated pointer to ICertView.
IEnumCERTVIEWROW * pEnumRow = NULL;
HRESULT    hr;

hr = pCertView->OpenView(&pEnumRow);
if (S_OK != hr)
    printf("Failed ICertView::OpenView - %x\n", hr);
else
    // use pEnumRow as needed, to enumerate data rows
    // ...
// Done processing, free resources.
if (NULL != pEnumRow)
    pEnumRow->Release();
```

## -see-also

<a href="/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>



<a href="/windows/desktop/api/certview/nn-certview-icertview2">ICertView2</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">ICertView::OpenConnection</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewrow">IEnumCERTVIEWROW</a>



<a href="/windows/desktop/api/certview/nf-certview-ienumcertviewrow-next">IEnumCERTVIEWROW::Next</a>