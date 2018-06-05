---
UID: NS:htmlhelp.tagHH_AKLINK
title: tagHH_AKLINK
author: windows-sdk-content
description: Use this structure to specify one or more ALink names or KLink keywords that you want to search for.
old-location: htmlhelp\hh_aklink_structure.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconstrhhaklink.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: HH_AKLINK, HH_AKLINK structure [HTML Help Workshop], htmlhelp.hh_aklink_structure, htmlhelp/HH_AKLINK, tagHH_AKLINK, vsconStrhhaklink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: htmlhelp.h
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
tech.root: 
req.typenames: HH_AKLINK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	HtmlHelp.h
api_name:
-	HH_AKLINK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagHH_AKLINK structure


## -description


Use this structure to specify one or more ALink names or KLink keywords that you want to search for.


## -struct-fields




### -field cbStruct

Specifies the size of the structure. This value must always be filled in before passing the structure to the HTML Help API. 


### -field fReserved

This parameter must be set to FALSE. 


### -field pszKeywords

Specifies one or more ALink names or KLink keywords to look up. Multiple entries are delimited by a semicolon. 


### -field pszUrl

Specifies the topic file to navigate to if the lookup fails. <i>pszURL</i> refers to a <a href="https://msdn.microsoft.com/DB3F1302-6933-45e8-9AF7-E3C075549B51">valid topic</a> within the specified compiled help (.chm) file and does not support Internet protocols that point to an HTML file. 


### -field pszMsgText

Specifies the text to display in a message box if the lookup fails and <i>fIndexOnFail</i> is FALSE and <i>pszURL</i> is NULL. 


### -field pszMsgTitle

Specifies the caption of the message box in which the <i>pszMsgText</i> parameter appears. 


### -field pszWindow

Specifies the name of the window type in which to display one of the following: 


<ul>
<li>The selected topic, if the lookup yields one or more matching topics.</li>
<li>The topic specified in <i>pszURL</i>, if the lookup fails and a topic is specified in <i>pszURL</i>.</li>
</ul>
The Index tab, if the lookup fails and <i>fIndexOnFail</i> is specified as TRUE.


### -field fIndexOnFail

Specifies whether to display the keyword in the Index tab of the HTML Help Viewer if the lookup fails. The value of <i>pszWindow</i> specifies the Help Viewer. 


## -remarks



<ul>
<li>ALink name and KLink keyword lookups are case sensitive, and multiple keywords are delimited by a semicolon.</li>
<li>If the lookup yields one or more matching topics, the topic titles appear in the Topics Found dialog box.</li>
</ul>
If the lookup yields no matching topics, <b>HtmlHelp()</b> checks the values of the following <b>HH_AKLINK</b> members to determine what alternative action to take: 

<ul>
<li><i>fIndexOnFail</i>. If <i>fIndexOnFail</i> is TRUE, the Index tab is selected in the help window specified in <i>pszWindow</i>, and the keyword specified in <i>pszKeyword</i> is selected in the entry field. </li>
<li><i>pszURL</i>. If <i>fIndexOnFail</i> is FALSE, the topic file specified in <i>pszURL</i> appears in the help window specified in <i>pszWindow</i>. </li>
<li><i>pszMsgText</i> and <i>pszMsgTitle</i>. If <i>fIndexOnFail</i> is FALSE and <i>pszURL</i> is NULL, a message box appears using the text and caption specified in <i>pszMsgText</i> and <i>pszMsgTitle</i>. </li>
</ul>
<h3><a id="Used_by"></a><a id="used_by"></a><a id="USED_BY"></a>Used by</h3>
<ul>
<li>
<a href="https://msdn.microsoft.com/E9BA3037-1402-4021-A1BB-B15774AAD5A3">HH_ALINK_LOOKUP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/F91C9EB5-6660-47bd-AA8D-484B4E0DF1F6">HH_KEYWORD_LOOKUP</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/E75CA82E-9759-47d8-AF84-5842EDAB019D">About Structures</a>
 

 

