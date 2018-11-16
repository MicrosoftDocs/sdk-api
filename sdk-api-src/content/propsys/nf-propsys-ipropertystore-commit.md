---
UID: NF:propsys.IPropertyStore.Commit
title: IPropertyStore::Commit
author: windows-sdk-content
description: Saves a property change.
old-location: properties\IPropertyStore_Commit.htm
tech.root: properties
ms.assetid: 25b6913e-e630-4cae-b155-d9d475593c9e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Commit, Commit method [Windows Properties], Commit method [Windows Properties],IPropertyStore interface, IPropertyStore interface [Windows Properties],Commit method, IPropertyStore.Commit, IPropertyStore::Commit, properties.IPropertyStore_Commit, propsys/IPropertyStore::Commit, shell.IPropertyStore_Commit, shell_IPropertyStore_Commit, shell_IPropertyStoreshell_IPropertyStore_Commit_cpp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - Propsys.h
api_name:
 - IPropertyStore.Commit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- propsys.h
: 
- IPropertyStore.Commit
: 
---

# IPropertyStore::Commit


## -description


Saves a property change.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> or <b>INPLACE_S_TRUNCATED</b> if successful, or an error value otherwise, including the following:

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
All of the property changes were successfully written to the stream or path. This includes the case where no changes were pending and nothing was written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INPLACE_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The value was set but truncated in a string value or rounded if a numeric value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The stream or file is read-only so the method was not able to set the value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The property handler could not store any value for the <a href="shell.PROPERTYKEY">PROPERTYKEY</a>  specified. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Some or all of the changes could not be written to the file. Another appropriate error code can be used in place of E_FAIL.

</td>
</tr>
</table>
 




## -remarks



Before it returns, <a href="shell.IPropertyStore_Commit">Commit</a> releases the file stream or path with which the handler was initialized. Therefore, no <a href="shell.IPropertyStore">IPropertyStore</a> methods succeed after <b>Commit</b>. At that point, they return E_FAIL.


<a href="shell.Building_Property_Handlers_Property_Handlers">Initializing Property Handlers</a> must ensure that property changes result in a valid destination file, even if the <a href="shell.IPropertyStore_Commit">Commit</a> process terminates abnormally or otherwise encounters an error. Handlers initialized through <a href="https://msdn.microsoft.com/9050845d-1e70-4e85-8d2f-c8bbb382abe5">IInitializeWithStream</a> can do this easily because the stream <i>pstream</i> passed to <a href="https://msdn.microsoft.com/1e04c0a4-aa9b-4e2c-8307-525809ca903f">Initialize</a> implements copy-on-write behavior—explained below—by default.



<table class="clsStd">
<tr>
<td>Property handlers that use <a href="https://msdn.microsoft.com/9050845d-1e70-4e85-8d2f-c8bbb382abe5">IInitializeWithStream</a> and automatic safe-save.</td>
<td>When the handler implementation first calls <i>pstream</i>-&gt;<a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">Write</a>, the modified source stream is copied to a destination stream. When the handler subsequently calls <a href="https://msdn.microsoft.com/335c3a53-ca6a-42f3-bbf9-684ed48591e6">IStream::Commit</a>, the source stream is automatically replaced with the destination, ensuring a valid file. This copy-on-write behavior is completely automatic from the point of view of the handler author for handlers that use <a href="https://msdn.microsoft.com/9050845d-1e70-4e85-8d2f-c8bbb382abe5">IInitializeWithStream</a>.</td>
</tr>
<tr>
<td>Property handlers that use <a href="https://msdn.microsoft.com/323181ab-1dc2-4b2a-a91f-3eccd7968bcd">IInitializeWithFile</a>.</td>
<td>A handler initialized with <a href="https://msdn.microsoft.com/323181ab-1dc2-4b2a-a91f-3eccd7968bcd">IInitializeWithFile</a> is responsible for ensuring that updates to the file as a result of writing property changes do not result in a corrupt file. Whenever property changes require the rewriting of a large part of the file, the handler should make changes to a new destination file and then automatically replace the source file through the <a href="https://msdn.microsoft.com/23402a71-e945-4891-9815-c75e57051501">ReplaceFile</a> function.</td>
</tr>
<tr>
<td>Property handlers that use <a href="https://msdn.microsoft.com/9050845d-1e70-4e85-8d2f-c8bbb382abe5">IInitializeWithStream</a> and manual safe-save.</td>
<td>The default copy-on-write behavior provided by <a href="https://msdn.microsoft.com/1e04c0a4-aa9b-4e2c-8307-525809ca903f">Initialize</a> causes the entire source stream to be duplicated during a write operation. This can be costly for large streams, especially when a large portion of the stream is to be changed. An alternative for the property handler author is to manually ensure that property changes do not corrupt the stream in case of failure. To do this, the author marks the handler as ManualSafeSave in the handler's CoClass registry subkey and queries the stream for <a href="https://msdn.microsoft.com/7cedf8eb-b4ef-4889-bd7b-a734e939e872">IDestinationStreamFactory</a>.</td>
</tr>
</table>
 


<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <i>{00000000-0000-0000-0000-000000000000}</i>
         (Default) = Sample Property Handler
         <b>ManualSafeSave [REG_DWORD]</b> = 0x0001</pre>


A handler marked with ManualSafeSave can also opt to do a fast in-place save operation if writing the property changes does not require a change in the size of the stream. To do this, the handler writes to the source stream and then calls <a href="https://msdn.microsoft.com/335c3a53-ca6a-42f3-bbf9-684ed48591e6">IStream::Commit</a>. Do not attempt this if the property changes require a change in the size of the stream. This can result in a corrupt file stream if the process should terminate abnormally or if an unexpected error should occur.



