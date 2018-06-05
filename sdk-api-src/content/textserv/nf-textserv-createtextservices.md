---
UID: NF:textserv.CreateTextServices
title: CreateTextServices function
author: windows-sdk-content
description: The CreateTextServices function creates an instance of a text services object. The text services object supports a variety of interfaces, including ITextServices and the Text Object Model (TOM).
old-location: controls\CreateTextServices.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolfunctions\createtextservices.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CreateTextServices, CreateTextServices function [Windows Controls], _win32_CreateTextServices, _win32_CreateTextServices_cpp, controls.CreateTextServices, controls._win32_CreateTextServices, textserv/CreateTextServices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msftedit.dll
api_name:
-	CreateTextServices
product: Windows
targetos: Windows
req.lib: Riched20.lib
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CreateTextServices function


## -description


The <b>CreateTextServices</b> function creates an instance of a text services object. The text services object supports a variety of interfaces, including <a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a> and the 
			Text Object Model (TOM).


## -parameters




### -param punkOuter [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the outer object if the text services object is being created as part of an aggregate object. This parameter can be <b>NULL</b> if the object is not part of an aggregate. 


### -param pITextHost [in]

Type: <b><a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>*</b>

Pointer to your implementation of the <a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a> interface. This pointer must not be <b>NULL</b>. 


### -param ppUnk [out]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Pointer to a variable that receives a pointer to the private <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the text services object. You can call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on this pointer to retrieve <a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a> or <a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a> interface pointers. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the text services object was created successfully, the return value is S_OK. 

If the function fails, one of the following COM error codes are returned. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory for text services object could not be allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The text services object could not be initialized.

</td>
</tr>
</table>
 




## -remarks



A text services object can be created as part of a standard COM-aggregated object. If it is, then callers should follow standard OLE32 rules for dealing with aggregated objects and caching interface pointers obtained through <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> from the private <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

