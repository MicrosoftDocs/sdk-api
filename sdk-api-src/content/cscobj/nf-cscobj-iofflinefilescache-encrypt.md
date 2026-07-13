---
UID: NF:cscobj.IOfflineFilesCache.Encrypt
title: IOfflineFilesCache::Encrypt (cscobj.h)
description: Encrypts or unencrypts the contents of the Offline Files cache cached for the calling user.
helpviewer_keywords: ["Encrypt","Encrypt method [Offline Files]","Encrypt method [Offline Files]","IOfflineFilesCache interface","IOfflineFilesCache interface [Offline Files]","Encrypt method","IOfflineFilesCache.Encrypt","IOfflineFilesCache::Encrypt","OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_ASYNCPROGRESS","OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_BACKGROUND","OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_CONSOLE","OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_INTERACTIVE","OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_LOWPRIORITY","cscobj/IOfflineFilesCache::Encrypt","of.iofflinefilescache_encrypt"]
old-location: of\iofflinefilescache_encrypt.htm
tech.root: of
ms.assetid: b7531018-4837-4fde-8947-0f099f6de9e5
ms.date: 12/05/2018
ms.keywords: Encrypt, Encrypt method [Offline Files], Encrypt method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],Encrypt method, IOfflineFilesCache.Encrypt, IOfflineFilesCache::Encrypt, OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_ASYNCPROGRESS, OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_BACKGROUND, OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_CONSOLE, OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_INTERACTIVE, OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_LOWPRIORITY, cscobj/IOfflineFilesCache::Encrypt, of.iofflinefilescache_encrypt
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesCache::Encrypt
 - cscobj/IOfflineFilesCache::Encrypt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesCache.Encrypt
---

# IOfflineFilesCache::Encrypt


## -description

Encrypts or unencrypts the contents of the Offline Files cache cached for the calling user.  When the cache is encrypted, all files subsequently cached are automatically encrypted.  When the cache is unencrypted, all files subsequently cached are cached unencrypted.

Existing files in the cache are either encrypted or unencrypted to match the new state of the cache.

## -parameters

### -param hwndParent [in]

Identifies the parent window for any user interface elements displayed. This parameter is ignored if the <b>OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_INTERACTIVE</b> flag is not set in the <i>dwEncryptionControlFlags</i> parameter.

### -param bEncrypt [in]

<b>TRUE</b> to encrypt, <b>FALSE</b> to unencrypt.

### -param dwEncryptionControlFlags [in]

This parameter can be one or more of the following values.



#### OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_LOWPRIORITY (0x00000200)

Reserved for future use.



#### OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_ASYNCPROGRESS (0x00000400)

Progress is reported to the progress interface asynchronously with the actual operations.  For more information about behavior, see the Asynchronous Progress Notifications section.  If this flag is not set, progress is reported synchronously with each operation.



#### OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_INTERACTIVE (0x00000800)

Set this flag if the operation is allowed to display user interface elements as necessary.  An example is the system's credential-request dialog.  If this flag is set, the value in <i>hwndParent</i> is used as the parent for any user interface elements displayed.



#### OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_CONSOLE (0x00001000)

This flag is ignored if the <b>OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_INTERACTIVE</b> flag is not set.  If the <b>OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_INTERACTIVE</b> flag is set, this flag indicates that any UI produced should be directed to the console window associated with the process invoking the operation.



#### OFFLINEFILES_ENCRYPTION_CONTROL_FLAG_BACKGROUND (0x00010000)

Set this flag if you want the encryption operation to avoid sharing violations in the event that an application wishes to open a file that is currently open for the encryption operation.  When that scenario occurs and this flag is set, the encryption operation immediately stops processing that particular file at that time.  This flag is primarily used by the Offline Files service when ensuring cache encryption at user logon.  Normally a client calling this method would not set this flag.

### -param bAsync [in]

Indicates whether the operation is to be performed asynchronously.  If this parameter is <b>TRUE</b>, the operation is scheduled for asynchronous operation and the function returns immediately.  If this parameter is <b>FALSE</b>, the function returns when the operation is complete.

### -param pIProgress [in]

Interface to an event sink that will receive progress events during the operation.  If events are not desired, this parameter may be <b>NULL</b>.  Note that this parameter is highly recommended for asynchronous operation.  A progress implementation is the only way to be notified when the asynchronous operation completes.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_CANCELLED)</code> if the operation is canceled.

## -remarks

Cancellation of this operation does not restore the cached files to their prior encryption state.  This may leave the cache in a partially encrypted or unencrypted state.  The same condition can occur if the operation is aborted due to an error.  To resolve the partial state, repeat the operation until successful completion.

Also note that the Offline Files service automatically performs the encryption operation in the background following user logon.  This ensures that all files cached by that user are in the correct state - encrypted or unencrypted – to match the state of the cache.

<table>
<tr>
<th>If canceled while...</th>
<th>Cache state is...</th>
<th>New cached files will be...</th>
</tr>
<tr>
<td>Encrypting</td>
<td>Partially encrypted</td>
<td>Encrypted</td>
</tr>
<tr>
<td>Unencrypting</td>
<td>Partially unencrypted</td>
<td>Unencrypted</td>
</tr>
</table>
 

The current encryption state of the Offline Files cache can be checked by using the Offline Files Control Panel or by calling <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-getencryptionstatus">IOfflineFilesCache::GetEncryptionStatus</a>.

The caller can implement the progress callback methods in the following list to obtain the progress information for each processed file and directory.

<table>
<tr>
<th>Progress Events Interface</th>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesprogress-begin">Begin</a>
</td>
<td>Called at the start of the operation.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessimpleprogress">IOfflineFilesSimpleProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessimpleprogress-itembegin">ItemBegin</a>
</td>
<td>Called at the start of processing for each file.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessimpleprogress">IOfflineFilesSimpleProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessimpleprogress-itemresult">ItemResult</a>
</td>
<td>Called after each file is encrypted.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesprogress-queryabort">QueryAbort</a>
</td>
<td>Called periodically during the sync operation to detect a request for cancellation.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesprogress-end">End</a>
</td>
<td>Called at the end of the operation.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>