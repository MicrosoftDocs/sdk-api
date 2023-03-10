---
UID: NN:txlogpub.ILog
title: ILog (txlogpub.h)
description: Provides generic low-level logging functionality.
helpviewer_keywords: ["ILog","ILog interface [COM]","ILog interface [COM]","described","_com_ilog","com.ilog","txlogpub/ILog"]
old-location: com\ilog.htm
tech.root: com
ms.assetid: 93f2be99-0799-4047-ae4e-62f0e74d15c3
ms.date: 12/05/2018
ms.keywords: ILog, ILog interface [COM], ILog interface [COM],described, _com_ilog, com.ilog, txlogpub/ILog
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILog
 - txlogpub/ILog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Txlogpub.h
api_name:
 - ILog
---

# ILog interface


## -description

Provides generic low-level logging functionality.


The <a href="/previous-versions/windows/desktop/clfs/common-log-file-system-portal">Common Log File System</a> (CLFS), provides functionality that is a superset of that provided by <b>ILog</b>.

## -inheritance

The <b>ILog</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILog</b> also has these types of members:

## -remarks

WAL is a technique used by certain applications, such as database management systems, to implement atomic and isolated transactions. This technique involves writing records of changes to the application's resources to a log before you make these changes. This way the changes can be reverted if they are required, for example if the transaction fails or is interrupted. In order for applications to provide transactions that are robust against interruptions such as system crash or power failure, the logging implementation must provide a method for forcing the log; that is, to make sure that previously written records are on disk before continuing.



Writing records that use <b>ILog</b> is a sequential operation; that is, new records are always appended to the end of the log. Each record appended to the log is assigned a log sequence number (LSN), a numeric identifier which may be used to retrieve the record later. The data type LSN is a typedef for <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>, a signed 64-bit value; however, <b>ILog</b> uses only LSNs with nonnegative values. In addition, LSNs must satisfy the following conditions:



<ul>
<li>LSNs are monotonically increasing; if record B is written to the log after record A, the LSN of record B must be larger than the LSN of record A.
</li>
<li>Values of zero and MAXLSN (0x7FFFFFFFFFFFFFFF) must never be used as the LSN of a record, as they have special meaning to some of the methods of <b>ILog</b>.
</li>
</ul>
Other than the conditions here, no assumptions should be made about how LSNs are assigned by an implementation of <b>ILog</b>. In particular, it is not safe to assume that records will be assigned sequential values for LSNs.



After a record is appended to the log, it may not be modified. However, when previously written records are no longer needed, for example records of changes in a transaction that has already been committed, <b>ILog</b> supports truncating the log. This way, disk space that was used for nonessential records may be reused. Truncating the log consists of deleting all records with an LSN less than a specified value.



As a performance optimization, some implementations of <b>ILog</b> may buffer records in memory until the log is forced. If this is the case, special you must consider error control and recovery. Consider the following situation:

<ol>
<li>Record A is appended to the log, but the log is not forced. The <b>ILog</b> implementation copies the record to a buffer in memory and returns a success code.</li>
<li>Record B is appended to the log, and the <b>ILog</b> implementation decides to force the log to disk. This is either because the caller asked the log to be forced or because the memory buffer is full. However, the write operation fails, for example because of low disk space.</li>
</ol>
In this situation, it would be inappropriate for the <b>ILog</b> implementation to enable additional records to be appended to the log, unless it can guarantee that all records for which it returned a success code are first written to disk. One possible method of error control would be to pin the log in an error state when this situation occurs, permanently disallowing additional writes to the log instance. Callers that do not force the log to disk for each appended record should realize that this situation may occur and be able to handle it appropriately.

<h3><a id="ILog_File-based_Implementation"></a><a id="ilog_file-based_implementation"></a><a id="ILOG_FILE-BASED_IMPLEMENTATION"></a>ILog File-based Implementation</h3>
The Windows operating system provides a file-based implementation of <b>ILog</b>, which enables you to create a log suited for write-ahead logging on a file. The log uses a file as a circular buffer, which enables unused space to be reused. This may also increase the size of the file that may be needed to fit additional records when the log is full. Changes to the log are made atomically, so that the contents of the log may be recovered after a crash. This implementation uses a buffer in memory for appending log records. As a result, records are not guaranteed to be written to disk when the <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-appendrecord">ILog::AppendRecord</a> method returns, unless the caller requests that the log be forced.

Use the following CLSID to create an instance of a file based log (see <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>):

CLSID_SimpleFileBasedLog
({E16C0593-128F-11D1-97E4-00C04FB9618A}
).

The file based implementation of <b>ILog</b> additionally supports the <a href="/windows/desktop/api/txlogpub/nn-txlogpub-ifilebasedloginit">IFileBasedLogInit</a> and <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a> interfaces. Use <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ifilebasedloginit-initnew">IFileBasedLogInit::InitNew</a> to create a new log file. Use <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">IPersistFile::Load</a> to open an existing log file.

This implementation uses a simple error control policy. If any one of the methods fails because of an error on the file-system level, which includes a disk full error, the log is pinned in an error state. This prevents clients from appending additional records to the file or reading potentially bad records. To continue to use the log file, you must create a new instance of the log.

## -see-also

<a href="/windows/desktop/api/txlogpub/nn-txlogpub-ifilebasedloginit">IFileBasedLogInit</a>
