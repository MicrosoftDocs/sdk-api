---
UID: NF:certview.ICertView.EnumCertViewColumn
title: ICertView::EnumCertViewColumn
author: windows-sdk-content
description: Obtains an instance of a column-enumeration sequence for the database schema.
old-location: security\icertview2_enumcertviewcolumn.htm
tech.root: seccrypto
ms.assetid: a51162f9-cc3d-4f06-993a-e5c9f57dd8a1
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CCertView object [Security],EnumCertViewColumn method, CVRC_COLUMN_MASK, CVRC_COLUMN_RESULT, CVRC_COLUMN_SCHEMA, CVRC_COLUMN_VALUE, EnumCertViewColumn, EnumCertViewColumn method [Security], EnumCertViewColumn method [Security],CCertView object, EnumCertViewColumn method [Security],ICertView interface, EnumCertViewColumn method [Security],ICertView2 interface, ICertView interface [Security],EnumCertViewColumn method, ICertView.EnumCertViewColumn, ICertView2 interface [Security],EnumCertViewColumn method, ICertView2::EnumCertViewColumn, ICertView::EnumCertViewColumn, certview/ICertView2::EnumCertViewColumn, certview/ICertView::EnumCertViewColumn, security.icertview2_enumcertviewcolumn
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ICertView2.EnumCertViewColumn
 - ICertView.EnumCertViewColumn
 - CCertView.EnumCertViewColumn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertView::EnumCertViewColumn


## -description


The <b>EnumCertViewColumn</b> method obtains an instance of a column-enumeration sequence for the database schema.

Note that this enumeration sequence cannot be used to enumerate the column values, only the database schema. Use 
<a href="https://msdn.microsoft.com/78fd2431-c4c7-4df9-856a-69665fa8c063">IEnumCERTVIEWROW::EnumCertViewColumn</a> if you need to enumerate the data values of the columns.


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
 


### -param ppenum [out]

A pointer to a pointer of <a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a> type. This method fails if the <i>ppenum</i> parameter is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and *<i>ppenum</i> is set to a pointer of <a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a> type.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is an <a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a> object.




## -remarks



The 
<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a> object can be used to enumerate the view's columns and retrieve each column's information.




## -see-also




<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">EnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/0b6660ee-458f-457f-8a38-0d950aee2710">ICertView</a>



<a href="https://msdn.microsoft.com/c29f1db3-0cdf-463e-a202-47fbba8e1c81">ICertView2</a>
 

 

