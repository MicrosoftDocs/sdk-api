---
UID: NF:certview.ICertView.GetColumnCount
title: ICertView::GetColumnCount (certview.h)

description: Retrieves the number of columns in the view of the Certificate Services database.
old-location: security\icertview2_getcolumncount.htm
tech.root: SecCrypto
ms.assetid: 0297d8e3-5077-40da-88b7-adac252e0f1b

ms.date: 12/05/2018
ms.keywords: CCertView object [Security],GetColumnCount method, CVRC_COLUMN_MASK, CVRC_COLUMN_RESULT, CVRC_COLUMN_SCHEMA, CVRC_COLUMN_VALUE, GetColumnCount, GetColumnCount method [Security], GetColumnCount method [Security],CCertView object, GetColumnCount method [Security],ICertView interface, GetColumnCount method [Security],ICertView2 interface, ICertView interface [Security],GetColumnCount method, ICertView.GetColumnCount, ICertView2 interface [Security],GetColumnCount method, ICertView2::GetColumnCount, ICertView::GetColumnCount, certview/ICertView2::GetColumnCount, certview/ICertView::GetColumnCount, security.icertview2_getcolumncount
ms.topic: method
f1_keywords: 
 - "certview/ICertView2.GetColumnCount"
dev_langs:
 - c++
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
 - ICertView2.GetColumnCount
 - ICertView.GetColumnCount
 - CCertView.GetColumnCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertView::GetColumnCount


## -description


The <b>GetColumnCount</b> method retrieves the number of columns in the view of the Certificate Services database.


## -parameters




### -param fResultColumn [in]

Specifies the  column. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CVRC_COLUMN_SCHEMA"></a><a id="cvrc_column_schema"></a><dl>
<dt><b>CVRC_COLUMN_SCHEMA</b></dt>
</dl>
</td>
<td width="60%">
Schema column information.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_COLUMN_RESULT"></a><a id="cvrc_column_result"></a><dl>
<dt><b>CVRC_COLUMN_RESULT</b></dt>
</dl>
</td>
<td width="60%">
Result column information.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_COLUMN_VALUE"></a><a id="cvrc_column_value"></a><dl>
<dt><b>CVRC_COLUMN_VALUE</b></dt>
</dl>
</td>
<td width="60%">
Value column information.

</td>
</tr>
<tr>
<td width="40%"><a id="CVRC_COLUMN_MASK"></a><a id="cvrc_column_mask"></a><dl>
<dt><b>CVRC_COLUMN_MASK</b></dt>
</dl>
</td>
<td width="60%">
Column information mask.

</td>
</tr>
</table>
 


### -param pcColumn [out]

A pointer to a variable that contains the number of columns in the view. This function will fail if the <i>pcColumn</i> parameter is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pcColumn</i> parameter is set to the number of columns in the view.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of columns in the view.




## -remarks



This method is used to determine the number of columns in the view. The returned number  represents the count of a result set's columns if <i>fResultColumn</i> is <b>TRUE</b> or the count of the full database schema's columns if <i>fResultColumn</i> is <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview2">CCertView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-icertview-setresultcolumncount">ICertView::SetResultColumnCount</a>
 

 

