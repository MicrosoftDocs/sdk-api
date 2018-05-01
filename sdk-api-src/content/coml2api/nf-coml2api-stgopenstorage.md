---
UID: NF:coml2api.StgOpenStorage
title: StgOpenStorage function
author: windows-driver-content
description: Opens an existing root storage object in the file system.
old-location: stg\stgopenstorage.htm
old-project: Stg
ms.assetid: 5ff18dc8-b24f-42bb-8c32-efc4d3696687
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: StgOpenStorage, StgOpenStorage function [Structured Storage], _stg_stgopenstorage, coml2api/StgOpenStorage, stg.stgopenstorage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: coml2api.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
-	API-MS-Win-Core-Com-l2-1-1.dll
-	coml2.dll
api_name:
-	StgOpenStorage
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# StgOpenStorage function


## -description



			The <b>StgOpenStorage</b> function opens an existing root storage object in the file system. Use this function to open compound files. Do not use it to open directories, files, or summary catalogs. Nested storage objects can only be opened using their parent 
<a href="https://msdn.microsoft.com/f1f0564e-0ecd-4b73-8863-9d6b6746fd02">IStorage::OpenStorage</a> method.
<div class="alert"><b>Note</b>  Applications should use the new function, 
<a href="https://msdn.microsoft.com/4f2138fb-1f80-4345-a3cb-9c11023457b1">StgOpenStorageEx</a>, instead of 
<b>StgOpenStorage</b>, to take advantage of the enhanced  and Windows Structured Storage features. This function, 
<b>StgOpenStorage</b>, still exists for compatibility with applications running on Windows 2000.</div><div> </div>

## -parameters




### -param pwcsName [in]

A pointer to the path of the <b>null</b>-terminated Unicode string file that contains the storage object to open. This parameter is ignored if the <i>pstgPriority</i> parameter is not <b>NULL</b>.


### -param pstgPriority [in]

A pointer to the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface that should be <b>NULL</b>. If not <b>NULL</b>, this parameter is used as described below in the Remarks section.

After <b>StgOpenStorage</b> returns, the storage object specified in <i>pStgPriority</i> may have been released and should no longer be used.


### -param grfMode [in]

Specifies the access mode to use to open the storage object.


### -param snbExclude [in]

If not <b>NULL</b>, pointer to a block of elements in the storage to be excluded as the storage object is opened. The exclusion occurs regardless of whether a snapshot copy happens on the open. Can be <b>NULL</b>.


### -param reserved [in]

Indicates reserved for future use; must be zero.


### -param ppstgOpen [out]

A pointer to a 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>* pointer variable that receives the interface pointer to the opened storage.


## -returns




						The <b>StgOpenStorage</b> function can also return any file system errors or system errors wrapped in an <b>HRESULT</b>. For more information, see 
<a href="_com_error_handling_strategies">Error Handling Strategies</a> and 
<a href="_com_handling_unknown_errors">Handling Unknown Errors</a>.




## -remarks



The 
<b>StgOpenStorage</b> function opens the specified root storage object according to the access mode in the <i>grfMode</i> parameter, and, if successful, supplies an 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the opened storage object in the <i>ppstgOpen</i> parameter.

To support the simple mode for saving a storage object with no substorages, the 
<b>StgOpenStorage</b> function accepts one of the following two flag combinations as valid modes in the <i>grfMode</i> parameter.

<pre class="syntax" xml:space="preserve"><code>    STGM_SIMPLE | STGM_READWRITE | STGM_SHARE_EXCLUSIVE</code></pre>
<pre class="syntax" xml:space="preserve"><code>    STGM_SIMPLE | STGM_READ | STGM_SHARE_EXCLUSIVE</code></pre>
To support the single-writer, multireader, direct mode, the first flag combination is the valid <i>grfMode</i> parameter for the writer.  The second flag combination is valid for readers.

<pre class="syntax" xml:space="preserve"><code>    STGM_DIRECT_SWMR | STGM_READWRITE | STGM_SHARE_DENY_WRITE</code></pre>
<pre class="syntax" xml:space="preserve"><code>    STGM_DIRECT_SWMR | STGM_READ | STGM_SHARE_DENY_NONE</code></pre>
In direct mode, one of the following three combinations are valid.

<pre class="syntax" xml:space="preserve"><code>    STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE</code></pre>
<pre class="syntax" xml:space="preserve"><code>    STGM_DIRECT | STGM_READ | STGM_SHARE_DENY_WRITE</code></pre>
<pre class="syntax" xml:space="preserve"><code>    STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE</code></pre>
<div class="alert"><b>Note</b>  Opening a storage object in read/write mode without denying write permission to others (the <i>grfMode</i> parameter specifies STGM_SHARE_DENY_WRITE) can be a time-consuming operation because the 
<b>StgOpenStorage</b> call must make a snapshot of the entire storage object.</div>
<div> </div>
Applications often try to open storage objects with the following access permissions. If the application succeeds, it never needs to make a snapshot copy.

<pre class="syntax" xml:space="preserve"><code>STGM_READWRITE | STGM_SHARE_DENY_WRITE 
    // transacted versus direct mode omitted for exposition </code></pre>
The application can revert to using the permissions and make a snapshot copy, if the previous access permissions fail. The application should prompt the user before making a time-consuming copy.

<pre class="syntax" xml:space="preserve"><code>STGM_READWRITE 
    // transacted versus direct mode omitted for exposition </code></pre>
If the document-sharing semantics implied by the access modes are appropriate, the application could try to open the storage as follows. In this case, if the application succeeds, a snapshot copy will not have been made (because <b>STGM_SHARE_DENY_WRITE</b> was specified, denying others write access).

<pre class="syntax" xml:space="preserve"><code>STGM_READ | STGM_SHARE_DENY_WRITE 
    // transacted versus direct mode omitted for exposition </code></pre>
<div class="alert"><b>Note</b>  To reduce the expense of making a snapshot copy, applications can open storage objects in priority mode (<i>grfMode</i> specifies <b>STGM_PRIORITY</b>).</div>
<div> </div>
The <i>snbExclude</i> parameter specifies a set of element names in this storage object that are to be emptied as the storage object is opened: streams are set to a length of zero; storage objects have all their elements removed. By excluding certain streams, the expense of making a snapshot copy can be significantly reduced. Almost always, this approach is used after first opening the storage object in priority mode, then completely reading the now-excluded elements into memory. This earlier priority-mode opening of the storage object should be passed through the <i>pstgPriority</i> parameter to remove the exclusion implied by priority mode. The calling application is responsible for rewriting the contents of excluded items before committing. Thus, this technique is most likely useful only to applications whose documents do not require constant access to their storage objects while they are active.

The <i>pstgPriority</i> parameter is intended as a convenience for callers replacing an existing storage object, often one opened in priority mode, with a new storage object opened on the same file but in a different mode. When <i>pstgPriority</i> is not <b>NULL</b>, it is used to specify the file name instead of <i>pwcsName</i>, which is ignored. However, it is recommended that applications always pass <b>NULL</b> for <i>pstgPriority</i> because <b>StgOpenStorage</b> releases the object under some circumstances, and does not release it under other circumstances.  In particular, if the function returns a failure result, it is not possible for the caller to determine whether or not the storage object was released.

The functionality of the <i>pstgPriority</i> parameter can be duplicated by the caller in a safer manner as shown in the following example:

<pre class="syntax" xml:space="preserve"><code>// Replacement for:
// HRESULT hr = StgOpenStorage(
//         NULL, pstgPriority, grfMode, NULL, 0, &amp;pstgNew);

STATSTG statstg;
HRESULT hr = pstgPriority-&gt;Stat(&amp;statstg, 0);
pStgPriority-&gt;Release();
pStgPriority = NULL;
if (SUCCEEDED(hr))
{
    hr = StgOpenStorage(statstg.pwcsName, NULL, grfMode, NULL, 0, &amp;pstgNew);
}     
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>



<a href="https://msdn.microsoft.com/3292484b-8eff-438d-b989-b58ae323872b">StgCreateDocfile</a>



<a href="https://msdn.microsoft.com/4f2138fb-1f80-4345-a3cb-9c11023457b1">StgOpenStorageEx</a>
 

 

