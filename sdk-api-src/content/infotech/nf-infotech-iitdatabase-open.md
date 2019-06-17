---
UID: NF:infotech.IITDatabase.Open
title: IITDatabase::Open (infotech.h)
author: windows-sdk-content
description: Opens a database.
old-location: htmlhelp\iitdatabase_open.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitdatabaseopen.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IITDatabase interface [HTML Help Workshop],Open method, IITDatabase.Open, IITDatabase::Open, Open, Open method [HTML Help Workshop], Open method [HTML Help Workshop],IITDatabase interface, htmlhelp.iitdatabase_open, infotech/IITDatabase::Open, refIITDatabaseOpen
ms.topic: method
f1_keywords: ["infotech/IITDatabase.Open"]
req.header: infotech.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITDatabase.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IITDatabase::Open


## -description


Opens a database.




## -parameters




### -param lpszHost [in]

Host name. You can pass NULL if calling the <b>Open</b> method locally, otherwise this string should contain the host description string, described below.


### -param lpszMoniker [in]

Name of database file to open. This should include the full path to the file name, if calling locally. If calling using HTTP, this should contain the ISAPI extension DLL name followed by the relative path to the database file, for example: 

<code>isapiext.dll?path1\path2\db.its</code>


### -param dwFlags [in]

Currently not used.




## -returns



This method can return one of these values.

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
The database was successfully opened.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E*</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface errors that can occur as storage is opened.



</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nn-infotech-iitdatabase">IITDatabase</a>
 

 

